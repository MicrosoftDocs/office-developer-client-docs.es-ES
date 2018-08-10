---
title: Almacenamiento estructurado en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 462ee84d5e9acd26f80bae6516179f21651749be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820795"
---
# <a name="structured-storage-in-mapi"></a>Almacenamiento estructurado en MAPI

  
  
**Hace referencia a**: Outlook 
  
Almacenamiento estructurado hace referencia a la organización jerárquica de almacenamiento de información que se introdujo con COM. En un entorno de almacenamiento estructurado, el almacenamiento se organiza en dos o tres tipos de objetos: 
  
- Objetos Stream
    
- Objetos de bytes de bloqueo
    
- Objetos de almacenamiento
    
Bytes de secuencia y bloqueo son objetos de nivel inferior que tener acceso directamente a los datos. Objetos Stream de implementan la interfaz **IStream** que define los métodos para leer, escribir, posicionamiento y acciones como copiar bytes de datos. Bloquear bytes objetos implementan otra interfaz COM, **ILockBytes**, para tener acceso a datos con una matriz de bytes. Matrices de bytes se suelen usar para proporcionar acceso personalizado a almacenamiento subyacente.
  
Objetos de almacenamiento se coloca sobre los objetos de bytes de secuencia o bloqueo; que pueden contener uno o varios de estos objetos, así como otros objetos de almacenamiento. Objetos de almacenamiento implementan la interfaz de **IStorage** que define los métodos para crear, obtener acceso a y mantener los objetos anidados. 
  
Debido a que **IStream**, **ILockBytes**y **IStorage** son interfaces COM en lugar de interfaces MAPI, sus métodos devuelven valores de error de COM en lugar de MAPI. Los clientes y proveedores de servicios de llamar a métodos de estas interfaces deben usar la función de la API **MapStorageSCode** para traducir estos valores en valores de error MAPI. Para obtener más información, vea [MapStorageSCode](mapstoragescode.md).
  
Los clientes y proveedores de servicios de usan almacenamiento estructurado para trabajar con las propiedades que son demasiado grandes para mantener con los métodos **IMAPIProp** , cadena suelen ser grande y propiedades binarias. Una de las maneras comunes que los clientes o proveedores de servicios de obtener acceso a ellos es mediante la especificación de **IStream** o **IStorage** como el identificador de interfaz en una llamada al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Por ejemplo, los clientes llaman **OpenProperty** con **PR_ATTACH_DATA_BIN** como la etiqueta de propiedad y IID_IStream como el identificador de interfaz para tener acceso a datos adjuntos binarios en un mensaje. 
  
Los clientes y proveedores de servicios pueden implementar sus propios objetos stream y almacenamiento de información o llamar a funciones de la API para las implementaciones de acceso proporcionadas por MAPI o COM. Debido a que las implementaciones proporcionadas atender la mayoría de los casos, los clientes y proveedores de servicios con muy poca frecuencia necesitan crear sus propios. 
  
Cuando un cliente llama **OpenProperty** en un objeto MAPI para tener acceso a una de sus propiedades a través de un objeto de almacenamiento, el proveedor de servicios normalmente abrirá el objeto de almacenamiento en modo directo. Sin embargo, esto es típico en lugar de comportamiento necesario. Los clientes deben se presupone que todos los objetos de almacenamiento abiertos o creados por proveedores de servicios se negocian y requieren una llamada a **IStorage::Commit**. También debe recordar que los cambios realizados en los objetos de almacenamiento no estarán permanentes hasta que llame a **IMAPIProp::SaveChanges** después de la última **Confirmar** para guardar el objeto MAPI. Para obtener más información, vea [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI y COM proporcionan varias funciones de la API para definir ni obtener acceso a los objetos stream y almacenamiento de información. En la siguiente tabla, se describen las funciones usadas con más frecuencia.
  
**Funciones para obtener acceso a los objetos Stream y almacenamiento**

|**Función**|**Descripción**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crea un objeto de almacenamiento para obtener acceso a un objeto de bytes de secuencias o de bloqueo.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crea un objeto de mensaje para tener acceso a un objeto de almacenamiento.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crea un objeto stream para tener acceso a un archivo.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crea un objeto stream que contiene la versión comprimida o sin comprimir de un objeto stream que contiene el texto enriquecido de un mensaje.  <br/> |
   
 **Para recuperar los nombres de las secuencias de un determinado subalmacenamiento**
  
1. Llamar al método **IStorage::EnumElements** del subalmacenamiento para obtener una interfaz **IEnumSTATSTG** . 
    
2. Llame al método **IEnumSTATSTG::Next** con tantos estructuras **STATSTG** en un momento tal y como se puede. Si se solicita 100 a la vez, **siguiente** normalmente devolverá S_FALSE con el contenido de _pceltFetched_ establecido en el número que se recuperaron realmente. 
    
3. Verificación de las estructuras de **STATSTG** que se marcan con STGTY_STREAM. 
    
4. El parámetro _pwcsName_ la versión. 
    
 **Para crear un objeto de almacenamiento para obtener acceso a un objeto existente de bytes de secuencias o de bloqueo**
  
- Los clientes llaman [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Para crear un objeto de mensaje para tener acceso a un objeto de almacenamiento existente**
  
- Los clientes y proveedores de servicios de llamada [OpenIMsgOnIStg](openimsgonistg.md). El objeto de mensaje que se crea difiere de los objetos de mensaje que normalmente creados los proveedores de almacén de mensajes en que no admite todos los [IMessage: IMAPIProp](imessageimapiprop.md) métodos, como **IMessage::SubmitMessage**de la interfaz. Un parámetro de entrada opcional para **OpenIMsgOnIStg** es una función de devolución de llamada que se ajusta al prototipo [MSGCALLRELEASE](msgcallrelease.md) . Esta función se denomina por el nuevo objeto de mensaje cuando el recuento de referencia del mensaje llega a cero. Implementación de una función **MSGCALLRELEASE** puede ser útil para llevar a cabo el procesamiento final antes de quitar completamente el mensaje nuevo. 
    
[OpenStreamOnFile](openstreamonfile.md) normalmente se usa para almacenar los datos adjuntos del archivo porque crea una secuencia que lee y escribe en un archivo. **OpenProperty** con **PR_ATTACH_DATA_BIN** como la etiqueta de propiedad crea una secuencia para almacenar los datos adjuntos binarios. 
  
 **Para comprimir o descomprimir una secuencia que contiene el texto del mensaje en el formato de texto enriquecido**
  
- Los clientes llaman [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crea una secuencia que se ajusta a la secuencia RTF. La secuencia de contenedor no implementa todos los métodos **IStream** ; se excluyen los siguientes métodos: **Seek**, **SetSize**, **Revertir**, **métodos LockRegion**, **UnlockRegion**, **Stat**y **clon**. Esto es debido a que los objetos de secuencia creados por **WrapCompressedRTFStream** no admiten **SetSize** o **Stat**, no hay una forma sencilla de extender o recuperar su tamaño. Es la mejor estrategia seleccionar un tamaño de búfer razonable y leer o escribir en un bucle.
    
> [!NOTE]
> COM tiene una implementación de objeto de almacenamiento en función de una matriz de bytes que devuelve un objeto **IEnumSTATSTG** desde el método **EnumElements** que es problemático. En concreto, el método **QueryInterface** no funciona correctamente. Proveedores de servicios que implementan sus propios objetos de almacenamiento de información mediante la implementación de COM deben crear un contenedor fino para el objeto **IEnumSTATSTG** que reenvía las llamadas a los métodos **IEnumSTATSTG** subyacentes pero implementa su propio **AddRef **, **Versión**, **QueryInterface**y **clon** métodos. 
  

