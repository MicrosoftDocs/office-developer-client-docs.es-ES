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
  
El almacenamiento estructurado hace referencia a la organización jerárquica de almacenamiento introducida con COM. En un entorno de almacenamiento estructurado, el almacenamiento se organiza en dos o tres tipos de objetos: 
  
- Objetos Stream
    
- Bloquear objetos bytes
    
- Objetos de almacenamiento
    
Los bytes de secuencia y bloqueo son objetos de nivel inferior que tienen acceso directo a los datos. Los objetos Stream implementan la **interfaz IStream** que define métodos para leer, escribir, colocar y copiar bytes de datos. Los objetos de bytes de bloqueo implementan otra interfaz COM, **ILockBytes,** para tener acceso a los datos con una matriz de bytes. Las matrices de bytes suelen usarse para proporcionar acceso personalizado al almacenamiento subyacente.
  
Los objetos de almacenamiento se encuentran en capas encima de los objetos stream o lock bytes; pueden contener uno o varios de estos objetos, así como otros objetos de almacenamiento. Los objetos de almacenamiento implementan **la interfaz IStorage** que define métodos para crear, obtener acceso y mantener objetos anidados. 
  
Dado **que IStream**, **ILockBytes** e **IStorage** son interfaces COM en lugar de interfaces MAPI, sus métodos devuelven valores de error COM en lugar de valores MAPI. Los clientes y proveedores de servicios que llaman a métodos en estas interfaces deben usar la función DE API **MapStorageSCode** para traducir estos valores a valores de error MAPI. Para obtener más información, [vea MapStorageSCode](mapstoragescode.md).
  
Los clientes y proveedores de servicios usan almacenamiento estructurado para trabajar con propiedades demasiado grandes para mantener con los métodos **IMAPIProp,** normalmente propiedades binarias y de cadena de gran tamaño. Una de las maneras comunes en que los clientes o proveedores de servicios tienen acceso a ellos es especificando **IStream** o **IStorage** como identificador de interfaz en una llamada al método [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Por ejemplo, los clientes llaman a **OpenProperty** con **PR_ATTACH_DATA_BIN** como etiqueta de propiedad y IID_IStream como identificador de interfaz para obtener acceso a datos adjuntos binarios en un mensaje. 
  
Los clientes y proveedores de servicios pueden implementar sus propios objetos de flujo y almacenamiento o llamar a funciones api para obtener acceso a las implementaciones proporcionadas por MAPI o COM. Dado que las implementaciones proporcionadas sirven para la mayoría de los propósitos, los clientes y proveedores de servicios rara vez necesitan crear sus propios. 
  
Cuando un cliente llama a **OpenProperty** en un objeto MAPI para tener acceso a una de sus propiedades a través de un objeto de almacenamiento, el proveedor de servicios normalmente abrirá el objeto de almacenamiento en modo directo. Sin embargo, esto es típico en lugar de un comportamiento obligatorio. Los clientes deben suponer que todos los objetos de almacenamiento abiertos o creados por proveedores de servicios se transaccionan y requieren una llamada a **IStorage::Commit**. También deben recordar que los cambios en los objetos de almacenamiento no se realizarán de forma permanente hasta que llamen a **IMAPIProp::SaveChanges** después de la confirmación **final** para guardar el objeto MAPI. Para obtener más información, [vea IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI y COM proporcionan varias funciones api para definir o tener acceso a objetos de almacenamiento y secuencia. Las funciones que se usan habitualmente se describen en la tabla siguiente.
  
**Funciones para obtener acceso a objetos de flujo y almacenamiento**

|**Función**|**Descripción**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crea un objeto de almacenamiento para tener acceso a un objeto stream o lock bytes.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crea un objeto de mensaje para tener acceso a un objeto de almacenamiento.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crea un objeto de secuencia para tener acceso a un archivo.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crea un objeto de secuencia que contiene la versión comprimida o sin comprimir de una secuencia que contiene el texto enriquecido de un mensaje.  <br/> |
   
 **Para recuperar los nombres de las secuencias en un substorage determinado**
  
1. Llama al método **IStorage::EnumElements** del substorage para obtener una **interfaz IEnumSTATSTG.** 
    
2. Llama **a IEnumSTATSTG::Next** con tantas estructuras **STATSTG** a la vez como puedas. Si pides 100 a la vez, **Next** normalmente devolverá S_FALSE con el contenido de  _pceltFetched_ establecido en el número que se recuperó realmente. 
    
3. Comprueba las estructuras **STATSTG** que están marcadas con STGTY_STREAM. 
    
4. Libere el _parámetro pwcsName._ 
    
 **Para crear un objeto de almacenamiento para tener acceso a un objeto stream o lock bytes existente**
  
- Los clientes [llaman a HrIStorageFromStream](hristoragefromstream.md). 
    
 **Para crear un objeto de mensaje para tener acceso a un objeto de almacenamiento existente**
  
- Los proveedores de servicios y clientes [llaman a OpenIMsgOnIStg](openimsgonistg.md). El objeto de mensaje que se crea difiere de los objetos de mensaje que normalmente crean los proveedores de al almacenamiento de mensajes en que no admite todos los métodos de interfaz [IMessage : IMAPIProp,](imessageimapiprop.md) como **IMessage::SubmitMessage**. Un parámetro de entrada opcional para **OpenIMsgOnIStg** es una función de devolución de llamada que se ajusta al prototipo [MSGCALLRELEASE.](msgcallrelease.md) El nuevo objeto de mensaje llama a esta función cuando el recuento de referencias del mensaje alcanza cero. La implementación de **una función MSGCALLRELEASE** puede ser útil para realizar el procesamiento final antes de que el nuevo mensaje se quite por completo. 
    
[OpenStreamOnFile](openstreamonfile.md) se usa normalmente para almacenar datos adjuntos de archivos porque crea una secuencia que lee y escribe en un archivo. **OpenProperty** con **PR_ATTACH_DATA_BIN** etiqueta de propiedad crea una secuencia para almacenar datos adjuntos binarios. 
  
 **Para comprimir o descomprimir una secuencia que contiene texto del mensaje en el formato de texto enriquecido**
  
- Los clientes [llaman a WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crea una secuencia que encapsula la secuencia RTF. La secuencia contenedora no implementa todos los métodos **IStream;** Se excluyen los métodos siguientes: **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat** y **Clone**. Esto se debe a que los objetos de secuencia creados por **WrapCompressedRTFStream** no **admiten SetSize** o **Stat**, no hay una forma fácil de extender o recuperar su tamaño. La mejor estrategia es elegir un tamaño de búfer razonable y leer o escribir en un bucle.
    
> [!NOTE]
> COM tiene una implementación de objeto de almacenamiento basada en una matriz de bytes que devuelve un objeto **IEnumSTATSTG** del método **EnumElements** que es problemático. En particular, el **método QueryInterface** no funciona correctamente. Los proveedores de servicios que implementan sus propios objetos de almacenamiento mediante la implementación COM deben crear un contenedor fino para el objeto **IEnumSTATSTG** que reenvía llamadas a los métodos **subyacentes de IEnumSTATSTG** pero implementa sus propios **métodos AddRef**, **Release**, **QueryInterface** y **Clone.** 
  

