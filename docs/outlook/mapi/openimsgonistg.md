---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406524"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un nuevo [objeto IMessage](imessageimapiprop.md) encima de un objeto OLE **IStorage** existente, que se usará en una sesión de mensaje. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>Parameters

_lpMsgSess_
  
> [in] Puntero a un objeto de sesión de mensaje en el que se va a crear el nuevo objeto **IMessage**-on- **IStorage.** 
    
_lpAllocateBuffer_
  
> [in] Puntero a la [función MAPIAllocateBuffer,](mapiallocatebuffer.md) que se usará para asignar memoria. 
    
_lpAllocateMore_
  
> [in] Puntero a la [función MAPIAllocateMore,](mapiallocatemore.md) que se usará para asignar memoria adicional. 
    
_lpFreeBuffer_
  
> [in] Puntero a la [función MAPIFreeBuffer,](mapifreebuffer.md) que se usará para liberar memoria. 
    
_lpMalloc_
  
> [in] Puntero a un objeto de asignador de memoria que expone la **interfaz OLE IMalloc.** La **interfaz IMessage** debe usar este método de asignación al trabajar con interfaces como **IStorage** e **IStream**. 
    
_lpMapiSup_
  
> [in] Puntero opcional a un objeto de compatibilidad MAPI que un proveedor de servicios puede usar para llamar a los métodos de la [interfaz IMAPISupport : IUnknown.](imapisupportiunknown.md) 
    
_lpStg_
  
> [in, out] Puntero a un objeto OLE **IStorage** que está abierto y tiene permiso de solo lectura o lectura y escritura. Dado **que IMessage** no admite el acceso de solo escritura, **OpenIMsgOnIStg** no acepta un objeto de almacenamiento abierto en modo de solo escritura. 
    
_lpfMsgCallRelease_
  
> [in] Puntero opcional a una función de devolución de llamada basada en el prototipo [MSGCALLRELEASE](msgcallrelease.md) al que MAPI llamará después de la última versión del objeto **IMessage**-on- **IStorage.** 
    
_ulCallerData_
  
> [in] Datos de autor de la llamada guardados por MAPI con el **objeto IMessage**-on- **IStorage** y pasados a la función de devolución de llamada basada **en MSGCALLRELEASE.** Los datos proporcionan contexto sobre el **objeto IMessage** que se va a liberar y el objeto **IStorage** encima del que se creó. 
    
_ulFlags_
  
> [in] Máscara de bits de marcas usadas para controlar si se llama al método OLE **IStorage::Commit** cuando la aplicación cliente o el proveedor de servicios llama al método **IMessage::SaveChanges.** Se pueden establecer las siguientes marcas: 
    
IMSG_NO_ISTG_COMMIT 
  
> No se llamará al **método OLE IStorage::Commit** cuando el cliente o proveedor llame a [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Habilita la creación de archivos .msg Unicode. El archivo [IMessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en su [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) y admite propiedades Unicode. 
    
  > [!NOTE]
  > La MAPI_UNICODE solo se admite en esta función en Outlook 2003 o posterior. 
  
_lppMsg_
  
> [salida] Puntero a un puntero al objeto **IMessage** abierto. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Solo se puede tener acceso a los atributos de propiedad en objetos de propiedad, es decir, objetos que implementan la [interfaz IMAPIProp : IUnknown.](imapipropiunknown.md) Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, **OpenIMsgOnIStg** compila un [objeto IMessage : IMAPIProp](imessageimapiprop.md) encima del objeto OLE **IStorage.** Los atributos de propiedad de estos objetos se pueden establecer o modificar con [SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperarse con [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Una sesión de mensaje debe abrirse con [OpenIMsgSession antes](openimsgsession.md) de llamar a **OpenIMsgOnIStg.** Al proporcionar un parámetro  _lpMsgSess_ válido, se asegura de que el nuevo mensaje se crea en una sesión de mensaje para que se cierre cuando se cierre la sesión. Si  _lpMsgSess_ es NULL, el mensaje se crea independientemente de cualquier sesión de mensaje. Si la aplicación cliente o el proveedor de servicios que creó el mensaje no lo libera, así como todos sus datos adjuntos y tablas abiertas, la memoria se pierde y puede provocar que la aplicación finalice. 
  
MAPI usa las funciones apuntadas por  _lpAllocateBuffer_,  _lpAllocateMore_ y  _lpFreeBuffer_ para la mayoría de la asignación y desasignación de memoria, en particular para asignar memoria para su uso por las aplicaciones cliente al llamar a interfaces de objetos como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). Los punteros _lpAllocateBuffer_, _lpAllocateMore_ y _lpFreeBuffer_ son opcionales cuando se llama a la función **OpenIMsgOnIStg** con un parámetro _lpMapiSup válido._ 
  
Dado que se trata de un objeto OLE subyacente, MAPI también debe usar la asignación de memoria OLE. Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y la asignación de memoria OLE, vea  _referencia del programador OLE_. 
  
Si se proporciona un valor válido para _lpMapiSup,_ **IMessage** admite las marcas MAPI_DIALOG y ATTACH_DIALOG llamando al método [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para proporcionar una interfaz de usuario de progreso para los métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMessage::D eleteAttach.](imessage-deleteattach.md) Además, el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) intenta convertir identificadores de entrada a corto plazo en identificadores de entrada a largo plazo llamando al método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) y realizando llamadas al objeto de libreta de direcciones resultante. Si se pasa NULL para  _lpMapiSup,_ **IMessage** omite MAPI_DIALOG y ATTACH_DIALOG y almacena identificadores de entrada a corto plazo sin conversión. 
  
El **objeto IStorage** al que apunta el parámetro  _lpStg_ debe abrirse en el modo STGM_READ o STGM_READWRITE. Si se STGM_READWRITE modo de STGM_TRANSACTED, también se debe establecer el modo de STGM_TRANSACTED. 
  
La función de devolución de llamada a la que apunta el _parámetro lpfMsgCallRelease_ es opcional; si se proporciona, debe basarse en el prototipo de función [MSGCALLRELEASE.](msgcallrelease.md) La **interfaz IMessage** lo llama cuando el recuento de referencias del objeto **IMessage**-on- **IStorage** se establece en cero por la última llamada a su **método Release.** La función de devolución de llamada se usa normalmente para liberar la interfaz **IStorage** subyacente. **IMessage** no intentará obtener acceso al **objeto IStorage** al que apunta el parámetro  _lpStg_ después de realizar la devolución de llamada. 
  
Algunos clientes o proveedores pueden escribir datos adicionales en el objeto **IStorage** más allá de lo que el propio **IMessage** escribe cuando se llama al [método SaveChanges.](imapiprop-savechanges.md) El cliente o el proveedor pueden usar la marca IMSG_NO_ISTG_COMMIT para evitar que **IMessage** llame al método OLE **IStorage::Commit** mientras procesa una **llamada SaveChanges;** en este caso, el cliente o proveedor debe confirmar el objeto **IStorage** cuando se escriben los datos adicionales. Para ayudar en esto, la implementación de **IMessage** garantiza el nombre de todos los substorages que crea en el objeto **IStorage** a partir de la cadena "__", es decir, con dos guiones bajos. El cliente o el proveedor pueden evitar las colisiones de nombres manteniendo sus nombres de substorage fuera de este espacio de nombres. 
  
MAPI no define el comportamiento de varias operaciones abiertas realizadas en un subobjeto de un mensaje, como datos adjuntos, una secuencia o un mensaje incrustado. MAPI actualmente permite abrir un subobjeto que ya está abierto una vez más, pero MAPI realiza la operación de apertura incrementando el recuento de referencias para el objeto abierto existente y devolviendolo al cliente o proveedor que llamó al método [IMessage::OpenAttach](imessage-openattach.md) o [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Esto significa que el acceso solicitado para la primera operación abierta en un subobjeto es el acceso proporcionado para todas las operaciones abiertas posteriores, independientemente del acceso solicitado por las operaciones. 
  
El procedimiento correcto para colocar un mensaje en un archivo adjunto es llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con un identificador de interfaz de IID_IMessage. **OpenProperty** actualmente también admite la creación de datos adjuntos de mensajes disponibles directamente en la interfaz OLE **IStorage,** es decir, mediante el identificador IID_IStorage interfaz. El acceso a **IStorage** se admite para permitir una forma sencilla de colocar un documento Microsoft Word en un archivo adjunto sin convertirlo a o desde la interfaz **OLE IStream.** Sin embargo, es posible que **IMessage** no se comporte de forma predecible si **OpenIMsgOnIStg** pasa un puntero **IStorage** a los datos adjuntos y, a continuación, los objetos se liberan en el orden incorrecto. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI usa el **método OpenIMsgOnIStg** para abrir una interfaz IMessage en la parte superior de . MSG para que el archivo se pueda manipular con MAPI.  <br/> |
   
## <a name="see-also"></a>Vea también

- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

