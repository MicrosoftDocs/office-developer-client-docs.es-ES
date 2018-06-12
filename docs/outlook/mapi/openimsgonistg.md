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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818439"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Se aplica a**: Outlook 
  
Crea un nuevo objeto [IMessage](imessageimapiprop.md) encima de un objeto OLE **IStorage** existente, para usarse dentro de una sesión de mensajería. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
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

## <a name="parameters"></a>Sintaxis

_lpMsgSess_
  
> [entrada] Puntero a un objeto de sesión de mensaje dentro del cual el nuevo **IMessage**- en - objeto **IStorage** es que se creará. 
    
_lpAllocateBuffer_
  
> [entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria. 
    
_lpAllocateMore_
  
> [entrada] Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se usará para asignar memoria adicional. 
    
_lpFreeBuffer_
  
> [entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
_lpMalloc_
  
> [entrada] Puntero a un objeto del asignador de memoria exposición de la interfaz de OLE **IMalloc** . **La interfaz** debe usar este método de asignación al trabajar con interfaces como **IStorage** y **IStream**. 
    
_lpMapiSup_
  
> [entrada] Puntero opcional a un objeto de soporte técnico MAPI que puede usar un proveedor de servicios para llamar a los métodos de la [IMAPISupport: IUnknown](imapisupportiunknown.md) interfaz. 
    
_lpStg_
  
> [entrada, salida] Puntero a un objeto OLE **IStorage** que está abierto y tiene como de solo lectura o permisos de lectura y escritura. Debido a que **IMessage** no admite el acceso de sólo escritura, **OpenIMsgOnIStg** no acepta un objeto de almacenamiento abierto en modo de sólo escritura. 
    
_lpfMsgCallRelease_
  
> [entrada] Puntero opcional a una función de devolución de llamada según el prototipo [MSGCALLRELEASE](msgcallrelease.md) es MAPI para llamar a después de la última versión en el **IMessage**- en - objeto **IStorage** . 
    
_ulCallerData_
  
> [entrada] Datos del autor de la llamada guarda por MAPI con el objeto de **IStorage** **IMessage**- en - y se pasan a la **MSGCALLRELEASE** en función de función de devolución de llamada. Los datos proporcionan contexto sobre el objeto **IMessage** que se publica y el objeto de **IStorage** en la parte superior que se generó. 
    
_ulFlags_
  
> [entrada] Máscara de bits de indicadores que se utilizan para controlar si se llama al método OLE **IStorage::Commit** cuando la aplicación de cliente o el proveedor de servicios llama al método **IMessage::SaveChanges** . Se pueden establecer los siguientes indicadores: 
    
IMSG_NO_ISTG_COMMIT 
  
> El método OLE **IStorage::Commit** no es se llama cuando el cliente o el proveedor llama a [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE.
  
> Habilita la creación de archivos .msg de Unicode. El archivo [IMessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en su [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) y es compatible con propiedades de Unicode. 
    
  > [!NOTE]
  > El indicador MAPI_UNICODE sólo se admite en esta función en Outlook 2003 o superior. 
  
_lppMsg_
  
> [out] Puntero a un puntero al objeto **IMessage** abierto. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Sólo se pueden tener acceso a atributos de la propiedad en objetos property, es decir, objetos que implementan la [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz. Para hacer que las propiedades MAPI esté disponible en un objeto de almacenamiento estructurado OLE, se basa **OpenIMsgOnIStg** un [IMessage: IMAPIProp](imessageimapiprop.md) objeto en la parte superior del objeto OLE **IStorage** . Pueden establecer los atributos de propiedad en dichos objetos o modifica con [SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperar con [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Una sesión de mensajería se debe abrir con [OpenIMsgSession](openimsgsession.md) antes de llamar a **OpenIMsgOnIStg** . Proporcionar un parámetro válido _lpMsgSess_ realizar sures que se crea el nuevo mensaje dentro de una sesión de mensajería para que se cierra cuando se cierra la sesión. Si _lpMsgSess_ es NULL, el mensaje se crea independientemente de cualquier sesión de mensajería. Si la aplicación de cliente o el proveedor de servicio que creó el mensaje de la versión, así como todos sus datos adjuntos no y abrir tablas, memoria se pierde y puede provocar que se cierre la aplicación. 
  
MAPI utiliza las funciones que señala _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayoría de asignación de memoria y cancelación de asignación, en particular para asignar la memoria para su uso por las aplicaciones cliente al llamar a las interfaces de objeto Por ejemplo, [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). Los punteros _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ son opcionales cuando se llama a la función **OpenIMsgOnIStg** con un parámetro válido _lpMapiSup_ . 
  
Debido a que se trata de un objeto OLE subyacente, MAPI también debe usar la asignación de memoria OLE. Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y asignación de memoria OLE, vea la _referencia del programador de OLE_. 
  
Si se proporciona un valor válido para _lpMapiSup_, **IMessage** es compatible con los indicadores MAPI_DIALOG y ATTACH_DIALOG llamando al método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) para proporcionar una interfaz de usuario de progreso para el [IMAPIProp::CopyTo](imapiprop-copyto.md) y los métodos de [IMessage::DeleteAttach](imessage-deleteattach.md) . Además, el método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) intenta convertir los identificadores de entrada a corto plazo a los identificadores de entrada a largo plazo por una llamada al método [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) y realizar llamadas en el objeto resultante de la libreta de direcciones. Si se pasa NULL para _lpMapiSup_, **IMessage** omite MAPI_DIALOG y ATTACH_DIALOG y almacena los identificadores de entrada a corto plazo sin conversión. 
  
El objeto **IStorage** indicado por el parámetro _lpStg_ debe abrirse en modo STGM_READ o de STGM_READWRITE. Si se usa el modo de STGM_READWRITE, también se debe establecer el modo de STGM_TRANSACTED. 
  
La función de devolución de llamada indicada por el parámetro _lpfMsgCallRelease_ es opcional; Si se proporciona, se debe basar en el prototipo de función [MSGCALLRELEASE](msgcallrelease.md) . **La interfaz** llama cuando el recuento de referencia del objeto **IStorage** **IMessage**- en - se establece en cero por la última llamada a su método de **versión** . La función de devolución de llamada se usa con frecuencia para liberar la interfaz **IStorage** subyacente. **IMessage** no intentará tener acceso al objeto **IStorage** indicado por el parámetro _lpStg_ después de realizar la devolución de llamada. 
  
Algunos clientes o proveedores podrían escribir datos adicionales para el objeto **IStorage** más allá de qué **IMessage** propio escribe cuando se llama a su método [SaveChanges](imapiprop-savechanges.md) . El cliente o el proveedor puede usar la marca IMSG_NO_ISTG_COMMIT para impedir que una llamada al método OLE **IStorage::Commit** durante el procesamiento de una llamada **SaveChanges** ; **IMessage** en este caso el cliente o el proveedor debe propio confirmar el objeto **IStorage** cuando se escriben los datos adicionales. Para facilitar esto, la implementación **IMessage** garantías para el nombre de todos los substorages que crea en el objeto de **IStorage** comienzan con la cadena "__", es decir, con dos caracteres de subrayado. El cliente o el proveedor para evitar conflictos de nombres, mantener sus nombres subalmacenamiento fuera de este espacio de nombres. 
  
MAPI no define el comportamiento de varias operaciones open realizadas en un subobjetos de un mensaje, como un archivo adjunto, una secuencia o un mensaje incrustado. MAPI permite actualmente una subobjetos que ya está abierto para abrirse una vez más, pero MAPI se lleva a cabo la operación de apertura por incrementar el recuento de referencia para el objeto abierto existente y devolución para el cliente o el proveedor que llama la [IMessage::OpenAttach ](imessage-openattach.md)o [IMAPIProp::OpenProperty](imapiprop-openproperty.md) (método). Esto significa que el acceso solicitado para la primera operación de apertura en un subobjetos el acceso proporcionado para todas las operaciones de open subsiguientes, independientemente de la solicitada por las operaciones de access. 
  
El procedimiento correcto para colocar un mensaje en un archivo adjunto es llamar al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) con un identificador de interfaz de IID_IMessage. **OpenProperty** actualmente también admite la creación de datos adjuntos de mensajes disponibles directamente en la interfaz OLE **IStorage** , es decir, utilizando el identificador de la interfaz IID_IStorage. Se admite el acceso de **IStorage** para permitir que una forma sencilla de poner un documento de Microsoft Word en un archivo adjunto sin convertirlo a o desde la interfaz **IStream** OLE. Sin embargo, **IMessage** es posible que no se comportan de forma predecible si **OpenIMsgOnIStg** se pasa un puntero **IStorage** para los datos adjuntos y, a continuación, se liberan los objetos en el orden incorrecto. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI utiliza el método **OpenIMsgOnIStg** para abrir una interfaz en la parte superior de la. MSG de archivos para que el archivo se puede manipular con MAPI.  <br/> |
   
## <a name="see-also"></a>Ver también

- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

