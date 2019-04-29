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
ms.openlocfilehash: f58fa70e98841db5507323a63737f1df6c1b7a6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411753"
---
# <a name="structured-storage-in-mapi"></a>Almacenamiento estructurado en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El almacenamiento estructurado se refiere a la organización jerárquica de almacenamiento que se presenta con COM. En un entorno de almacenamiento estructurado, el almacenamiento se organiza en dos o tres tipos de objetos: 
  
- Objetos Stream
    
- Bloquear objetos bytes
    
- Objetos de almacenamiento
    
Los bytes de secuencia y bloqueo son objetos de nivel inferior que tienen acceso directo a los datos. Los objetos Stream implementan la interfaz **IStream** que define los métodos para leer, escribir, colocar y copiar bytes de datos. Bloquear objetos bytes implemente otra interfaz COM, **ILockBytes**, para tener acceso a datos con una matriz de bytes. Las matrices de bytes se suelen usar para proporcionar acceso personalizado al almacenamiento subyacente.
  
Los objetos de almacenamiento se encuentran en capas en la parte superior de los objetos Stream o Lock bytes; pueden contener uno o varios de estos objetos, así como otros objetos de almacenamiento. Los objetos de almacenamiento implementan la interfaz **IStorage** , que define los métodos para crear, tener acceso y mantener objetos anidados. 
  
Como **IStream**, **ILockBytes**y **IStorage** son interfaces com en lugar de interfaces MAPI, sus métodos devuelven valores de error de com en lugar de valores MAPI. Los clientes y los proveedores de servicios que llaman a métodos en estas interfaces deben usar la función API **MapStorageSCode** para convertir estos valores en valores de error de MAPI. Para obtener más información, vea [MapStorageSCode](mapstoragescode.md).
  
Los clientes y los proveedores de servicios usan almacenamiento estructurado para trabajar con propiedades que son demasiado grandes como para mantenerlas con los métodos **IMAPIProp** , normalmente grandes propiedades binarias y de cadena. Una de las formas comunes de que los clientes o proveedores de servicios obtengan acceso a ellos es especificando **IStream** o **IStorage** como identificador de interfaz en una llamada al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) . Por ejemplo, los clientes llaman a **OpenProperty** con **PR_ATTACH_DATA_BIN** como etiqueta de propiedad y IID_IStream como el identificador de interfaz para obtener acceso a datos adjuntos binarios en un mensaje. 
  
Los clientes y los proveedores de servicios pueden implementar sus propios objetos de flujo y almacenamiento o llamar a las funciones de la API para obtener acceso a las implementaciones proporcionadas por MAPI o COM. Como las implementaciones suministradas tienen la mayoría de propósitos, los clientes y los proveedores de servicios raramente tienen que crear los suyos propios. 
  
Cuando un cliente llama a **OpenProperty** en un objeto MAPI para tener acceso a una de sus propiedades a través de un objeto de almacenamiento, el proveedor de servicios normalmente abrirá el objeto de almacenamiento en modo directo. Sin embargo, esto es típico en lugar de un comportamiento necesario. Los clientes deben asumir que todos los objetos de almacenamiento abiertos o creados por los proveedores de servicios son de transacción y requieren una llamada a **IStorage:: commit**. También deben recordar que los cambios realizados en los objetos de almacenamiento no se harán permanentes hasta que llamen a **IMAPIProp:: SaveChanges** después de la **confirmación** final para guardar el objeto MAPI. Para obtener más información, vea [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
  
MAPI y COM proporcionan varias funciones de API para definir o tener acceso a los objetos de almacenamiento y de secuencia. Las funciones que se usan con frecuencia se describen en la siguiente tabla.
  
**Funciones para obtener acceso a los objetos de almacenamiento y de secuencia**

|**Función**|**Descripción**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crea un objeto de almacenamiento para obtener acceso a un objeto Stream o Lock bytes.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crea un objeto Message para tener acceso a un objeto de almacenamiento.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crea un objeto Stream para obtener acceso a un archivo.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crea un objeto Stream que contiene la versión comprimida o sin comprimir de una secuencia que contiene el texto enriquecido de un mensaje.  <br/> |
   
 **Para recuperar los nombres de las secuencias en un subalmacenamiento determinado**
  
1. Llame al método **IStorage:: EnumElements** del subalmacén para obtener una interfaz **IEnumSTATSTG** . 
    
2. Llame a **IEnumSTATSTG:: Next** con tantas estructuras de **STATSTG** a la vez como pueda. Si solicita 100 a la vez, a **continuación** , se devolverá S_FALSE con el contenido de _pceltFetched_ establecido en el número que se ha recuperado realmente. 
    
3. Busque las estructuras **STATSTG** que están marcadas con STGTY_STREAM. 
    
4. Libere el parámetro _pwcsName_ . 
    
 **Para crear un objeto de almacenamiento para obtener acceso a un objeto Stream existente o Lock bytes**
  
- Los clientes llaman a [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Para crear un objeto Message para tener acceso a un objeto de almacenamiento existente**
  
- Los proveedores de servicios y los clientes llaman a [OpenIMsgOnIStg](openimsgonistg.md). El objeto de mensaje que se crea difiere de los objetos de mensaje que normalmente crean los proveedores de almacenamiento de mensajes en que no admite todos los métodos de interfaz [IMessage: IMAPIProp](imessageimapiprop.md) , como **IMessage:: SubmitMessage**. Un parámetro de entrada opcional para **OpenIMsgOnIStg** es una función de devolución de llamada que se ajusta al prototipo [MSGCALLRELEASE](msgcallrelease.md) . El nuevo objeto de mensaje llama a esta función cuando el recuento de referencia del mensaje llega a cero. La implementación de una función **MSGCALLRELEASE** puede ser útil para realizar el procesamiento final antes de que se Quite completamente el nuevo mensaje. 
    
[OpenStreamOnFile](openstreamonfile.md) se usa normalmente para almacenar datos adjuntos de archivos porque crea una secuencia que lee y escribe en un archivo. **OpenProperty** con **PR_ATTACH_DATA_BIN** como etiqueta de propiedad crea una secuencia para almacenar datos adjuntos binarios. 
  
 **Para comprimir o descomprimir una secuencia que contiene el texto del mensaje en el formato de texto enriquecido**
  
- Los clientes llaman a [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crea un objeto Stream que contiene la secuencia de RTF. La secuencia de contenedor no implementa todos los métodos **IStream** ; se excluyen los siguientes métodos: **Seek**, **setSize**, **Revert**, **LockRegion**, **UnlockRegion**, **STAT**y **Clone**. Esto se debe a que los objetos Stream creados por **WrapCompressedRTFStream** no son compatibles con **setSize** o **STAT**, ya que no hay una forma sencilla de ampliar o recuperar su tamaño. La mejor estrategia es elegir un tamaño de búfer razonable y leer o escribir en un bucle.
    
> [!NOTE]
> COM tiene una implementación de objeto de almacenamiento basada en una matriz de bytes que devuelve un objeto **IEnumSTATSTG** del método **EnumElements** que es problemático. En concreto, el método **QueryInterface** no funciona correctamente. Los proveedores de servicios que implementan sus propios objetos de almacenamiento mediante la implementación COM deben crear un contenedor fino para el objeto **IEnumSTATSTG** que reenvía llamadas a los métodos subyacentes de **IEnumSTATSTG** , pero implementa su propio **AddRef **, **Release**, **QueryInterface**y **Clone** (métodos). 
  

