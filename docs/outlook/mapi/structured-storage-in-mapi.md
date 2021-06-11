---
title: Estructura Storage en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f58fa70e98841db5507323a63737f1df6c1b7a6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411753"
---
# <a name="structured-storage-in-mapi"></a>Estructura Storage en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El almacenamiento estructurado hace referencia a la organización jerárquica de almacenamiento introducida con COM. En un entorno de almacenamiento estructurado, el almacenamiento se organiza en dos o tres tipos de objetos: 
  
- Objetos Stream
    
- Bloquear objetos bytes
    
- Storage objetos
    
Los bytes stream y lock son objetos de nivel inferior que tienen acceso directo a los datos. Los objetos Stream implementan la **interfaz IStream** que define métodos para leer, escribir, colocar y copiar bytes de datos. Los objetos de bytes de bloqueo implementan otra interfaz COM, **ILockBytes,** para tener acceso a datos con una matriz de bytes. Las matrices de bytes se usan normalmente para proporcionar acceso personalizado al almacenamiento subyacente.
  
Storage objetos están en capas en la parte superior de los objetos bytes de secuencia o bloqueo; pueden contener uno o varios de estos objetos, así como otros objetos de almacenamiento. Storage implementan la **interfaz IStorage** que define métodos para crear, obtener acceso y mantener objetos anidados. 
  
Dado **que IStream,** **ILockBytes** e **IStorage** son interfaces COM en lugar de interfaces MAPI, sus métodos devuelven valores de error COM en lugar de valores MAPI. Los clientes y los proveedores de servicios que llaman a métodos en estas interfaces deben usar la función DE API **MapStorageSCode para** traducir estos valores a valores de error MAPI. Para obtener más información, [vea MapStorageSCode](mapstoragescode.md).
  
Los clientes y proveedores de servicios usan el almacenamiento estructurado para trabajar con propiedades demasiado grandes para mantener con los métodos **IMAPIProp,** normalmente propiedades binarias y de cadena de gran tamaño. Una de las maneras comunes en que los clientes o proveedores de servicios tienen acceso a ellos es especificando **IStream** o **IStorage** como identificador de interfaz en una llamada al método [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Por ejemplo, los clientes llaman a **OpenProperty** con **PR_ATTACH_DATA_BIN** como etiqueta de propiedad y IID_IStream como identificador de interfaz para obtener acceso a datos adjuntos binarios en un mensaje. 
  
Los clientes y proveedores de servicios pueden implementar sus propios objetos de flujo y almacenamiento o llamar a funciones api para obtener acceso a implementaciones proporcionadas por MAPI o COM. Dado que las implementaciones suministradas sirven para la mayoría de los propósitos, los clientes y los proveedores de servicios rara vez necesitan crear los suyos propios. 
  
Cuando un cliente llama a **OpenProperty** en un objeto MAPI para tener acceso a una de sus propiedades a través de un objeto de almacenamiento, el proveedor de servicios normalmente abrirá el objeto de almacenamiento en modo directo. Sin embargo, esto es típico en lugar de un comportamiento obligatorio. Los clientes deben asumir que todos los objetos de almacenamiento abiertos o creados por los proveedores de servicios se realizan y requieren una llamada a **IStorage::Commit**. También deben recordar que los cambios en los objetos de almacenamiento no se realizarán permanentemente hasta que llamen a **IMAPIProp::SaveChanges** después de la confirmación **final** para guardar el objeto MAPI. Para obtener más información, [vea IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI y COM proporcionan varias funciones api para definir o obtener acceso a objetos de almacenamiento y secuencia. Las funciones que se usan con frecuencia se describen en la tabla siguiente.
  
**Funciones para obtener acceso a Storage y objetos Stream**

|**Función**|**Descripción**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crea un objeto de almacenamiento para obtener acceso a un objeto bytes de secuencia o de bloqueo.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crea un objeto de mensaje para obtener acceso a un objeto de almacenamiento.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crea un objeto stream para obtener acceso a un archivo.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crea un objeto de secuencia que contiene la versión comprimida o sin comprimir de una secuencia que contiene el texto enriquecido de un mensaje.  <br/> |
   
 **Para recuperar los nombres de las secuencias de un substorage determinado**
  
1. Llame al método **IStorage::EnumElements** del substorage para obtener una **interfaz IEnumSTATSTG.** 
    
2. Llama **a IEnumSTATSTG::Next** con tantas estructuras **STATSTG** a la vez como puedas. Si pide 100 a la vez, **Next** normalmente devolverá S_FALSE con el contenido de  _pceltFetched_ establecido en el número que se recuperó realmente. 
    
3. Compruebe las estructuras **STATSTG** que están marcadas con STGTY_STREAM. 
    
4. Libere el _parámetro pwcsName._ 
    
 **Para crear un objeto de almacenamiento para tener acceso a un objeto de bytes de secuencia o de bloqueo existente**
  
- Los clientes llaman [a HrIStorageFromStream](hristoragefromstream.md). 
    
 **Para crear un objeto de mensaje para obtener acceso a un objeto de almacenamiento existente**
  
- Los proveedores de servicios y clientes [llaman a OpenIMsgOnIStg](openimsgonistg.md). El objeto de mensaje que se crea difiere de los objetos de mensaje que normalmente crean los proveedores de almacén de mensajes, ya que no admite todos los métodos de interfaz [IMessage : IMAPIProp,](imessageimapiprop.md) como **IMessage::SubmitMessage**. Un parámetro de entrada opcional para **OpenIMsgOnIStg** es una función de devolución de llamada que se ajusta al prototipo [MSGCALLRELEASE.](msgcallrelease.md) El nuevo objeto message llama a esta función cuando el recuento de referencias del mensaje alcanza cero. La implementación de **una función MSGCALLRELEASE** puede ser útil para realizar el procesamiento final antes de que se quite por completo el nuevo mensaje. 
    
[OpenStreamOnFile](openstreamonfile.md) se usa normalmente para almacenar datos adjuntos de archivos porque crea una secuencia que lee y escribe en un archivo. **OpenProperty** con **PR_ATTACH_DATA_BIN** como la etiqueta de propiedad crea una secuencia para almacenar datos adjuntos binarios. 
  
 **Para comprimir o descomprimir una secuencia que contiene texto de mensaje en el formato de texto enriquecido**
  
- Los clientes llaman [a WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crea una secuencia que encapsula la secuencia RTF. La secuencia contenedora no implementa todos los métodos **IStream;** se excluyen los siguientes métodos: **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat** y **Clone**. Esto se debe a que los objetos de secuencia creados por **WrapCompressedRTFStream** no admiten **SetSize** o **Stat**, no hay una forma fácil de ampliar o recuperar su tamaño. La mejor estrategia es elegir un tamaño de búfer razonable y leer o escribir en un bucle.
    
> [!NOTE]
> COM tiene una implementación de objeto de almacenamiento basada en una matriz de bytes que devuelve un objeto **IEnumSTATSTG** del método **EnumElements** que es problemático. En concreto, el **método QueryInterface** no funciona correctamente. Los proveedores de servicios que implementan sus propios objetos de almacenamiento mediante la implementación COM deben crear un contenedor fino para el objeto **IEnumSTATSTG** que reenvía llamadas a los métodos **IEnumSTATSTG** subyacentes, pero implementa sus propios **métodos AddRef,** **Release,** **QueryInterface** y **Clone.** 
  

