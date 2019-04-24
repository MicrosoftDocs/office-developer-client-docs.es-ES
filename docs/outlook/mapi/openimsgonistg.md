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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348618"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un nuevo objeto [IMessage](imessageimapiprop.md) encima de un objeto OLE **IStorage** existente, que se va a usar en una sesión de mensajes. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage. h  <br/> |
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
  
> a Puntero a un objeto de sesión de mensaje en el que se va a crear el nuevo objeto **IMessage**-on- **IStorage** . 
    
_lpAllocateBuffer_
  
> a Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se va a usar para asignar memoria. 
    
_lpAllocateMore_
  
> a Puntero a la función [MAPIAllocateMore](mapiallocatemore.md) , que se va a usar para asignar memoria adicional. 
    
_lpFreeBuffer_
  
> a Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria. 
    
_lpMalloc_
  
> a Puntero a un objeto de asignador de memoria que expone la interfaz OLE **IMalloc** . La interfaz **IMessage** necesita utilizar este método de asignación al trabajar con interfaces como **IStorage** y **IStream**. 
    
_lpMapiSup_
  
> a Puntero opcional a un objeto de compatibilidad de MAPI que puede usar un proveedor de servicios para llamar a los métodos de la interfaz [IMAPISupport: IUnknown](imapisupportiunknown.md) . 
    
_lpStg_
  
> [in, out] Puntero a un objeto **IStorage** de OLE que está abierto y tiene permiso de solo lectura o de lectura y escritura. Dado que **IMessage** no admite el acceso de solo escritura, **OpenIMsgOnIStg** no acepta un objeto de almacenamiento abierto en modo de solo escritura. 
    
_lpfMsgCallRelease_
  
> a Puntero opcional a una función de devolución de llamada basada en el prototipo [MSGCALLRELEASE](msgcallrelease.md) al que MAPI debe llamar tras la última versión en el objeto **IMessage**-on- **IStorage** . 
    
_ulCallerData_
  
> a Datos del autor de la llamada guardados por MAPI con el objeto **IMessage**-on- **IStorage** y pasados a la función de devolución de llamada basada en **MSGCALLRELEASE** . Los datos proporcionan contexto sobre el objeto **IMessage** que se va a liberar y el objeto **IStorage** en la parte superior en el que se creó. 
    
_ulFlags_
  
> a Máscara de la máscara utilizada para controlar si se llama al método OLE **IStorage:: commit** cuando la aplicación cliente o el proveedor de servicios llama al método **IMessage:: SaveChanges** . Se pueden establecer los siguientes indicadores: 
    
IMSG_NO_ISTG_COMMIT 
  
> El método OLE **IStorage:: commit** no se llamará cuando el cliente o el proveedor llame a [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Habilita la creación de archivos. MSG Unicode. El archivo [IMessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en su [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) y admite propiedades Unicode. 
    
  > [!NOTE]
  > La marca MAPI_UNICODE solo se admite en esta función en Outlook 2003 o posterior. 
  
_lppMsg_
  
> contempla Puntero a un puntero al objeto **IMessage** abierto. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Solo se puede tener acceso a los atributos de propiedad en objetos Property, es decir, objetos que implementan la interfaz [IMAPIProp: IUnknown](imapipropiunknown.md) . Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, **OpenIMsgOnIStg** genera un objeto [IMessage: IMAPIProp](imessageimapiprop.md) encima del objeto OLE **IStorage** . Los atributos de propiedad de dichos objetos pueden establecerse o modificarse con [SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperarse con [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Debe abrirse una sesión de mensajes con [OpenIMsgSession](openimsgsession.md) antes de llamar a **OpenIMsgOnIStg** . Proporcionar un parámetro _lpMsgSess_ válido Asegúrese de que el nuevo mensaje se crea dentro de una sesión de mensajes para que se cierre cuando se cierre la sesión. Si _lpMsgSess_ es null, el mensaje se crea independientemente de cualquier sesión de mensajes. Si la aplicación cliente o el proveedor de servicios que ha creado el mensaje no la libera, así como todos sus datos adjuntos y tablas abiertas, la memoria se pierde y puede provocar que la aplicación finalice. 
  
MAPI usa las funciones a las que apunta _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ para la mayor parte de la asignación y desasignación de memoria, en particular para asignar memoria para que la usen las aplicaciones cliente al llamar a las interfaces del objeto. como [IMAPIProp:: GetProps](imapiprop-getprops.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md). Los punteros _lpAllocateBuffer_, _lpAllocateMore_y _lpFreeBuffer_ son opcionales cuando se llama a la función **OpenIMsgOnIStg** con un parámetro _lpMapiSup_ válido. 
  
Como se trata de un objeto OLE subyacente, MAPI también necesita usar la asignación de memoria OLE. Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y la asignación de memoria OLE, vea la _Referencia del programador de OLE_. 
  
Si se proporciona un valor válido para _lpMapiSup_, **IMessage** admite los indicadores MAPI_DIALOG y ATTACH_DIALOG llamando al método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) para proporcionar una interfaz de usuario de progreso para el [IMAPIProp:: CopyTo](imapiprop-copyto.md) y [IMessage::D métodos eleteattach](imessage-deleteattach.md) . Además, el método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) intenta convertir los identificadores de entrada a corto plazo en identificadores de entrada a largo plazo llamando al método [IMAPISupport:: OpenAddressBook](imapisupport-openaddressbook.md) y realizando llamadas en el objeto de la libreta de direcciones resultante. Si se pasa NULL para _lpMapiSup_, **IMessage** omite MAPI_DIALOG y ATTACH_DIALOG y almacena los identificadores de entrada a corto plazo sin conversión. 
  
El objeto **IStorage** al que señala el parámetro _lpStg_ debe estar abierto en el modo STGM_READ o STGM_READWRITE. Si se usa el modo STGM_READWRITE, también debe establecerse el modo STGM_TRANSACTED. 
  
La función de devolución de llamada a la que señala el parámetro _lpfMsgCallRelease_ es opcional; Si se proporciona, debe basarse en el prototipo de función [MSGCALLRELEASE](msgcallrelease.md) . La interfaz **IMessage** la llama cuando el recuento de referencias del objeto **IMessage**-on- **IStorage** se establece en cero mediante la última llamada a su método **Release** . La función de devolución de llamada se usa normalmente para liberar la interfaz de **IStorage** subyacente. **IMessage** no intentará tener acceso al objeto **IStorage** señalado por el parámetro _lpStg_ después de realizar la devolución de llamada. 
  
Algunos clientes o proveedores pueden escribir datos adicionales en el objeto **IStorage** más allá de lo que **IMessage** escribe cuando se llama a su método [SaveChanges](imapiprop-savechanges.md) . El cliente o el proveedor puede usar la marca IMSG_NO_ISTG_COMMIT para impedir que **IMessage** llame al método OLE **IStorage:: commit** mientras procesa una llamada de **SaveChanges** ; en este caso, el cliente o el proveedor deben confirmar el objeto **IStorage** cuando se escriben los datos adicionales. Para ayudar a esto, la implementación de **IMessage** garantiza el nombre de todos los subalmacénes que crea en el objeto **IStorage** a partir de la cadena "_ _", es decir, con dos guiones bajos. El cliente o proveedor puede evitar conflictos de nombres manteniendo sus nombres de subalmacén en este espacio de nombres. 
  
MAPI no define el comportamiento de varias operaciones de apertura realizadas en un subobjeto de un mensaje, como datos adjuntos, una secuencia o un mensaje incrustado. Actualmente MAPI permite que un subobjeto que ya está abierto se abra una vez más, pero MAPI realiza la operación de apertura incrementando el recuento de referencias para el objeto abierto existente y devolviéndolo al cliente o proveedor que llama al [IMessage:: OpenAttach ](imessage-openattach.md)o [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) método. Esto significa que el acceso solicitado para la primera operación de apertura en un subobjeto es el acceso proporcionado para todas las operaciones posteriores a la apertura, independientemente del acceso solicitado por las operaciones. 
  
El procedimiento correcto para colocar un mensaje en datos adjuntos es llamar al método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) con un identificador de interfaz de IID_IMessage. Actualmente, **OpenProperty** también admite la creación de datos adjuntos de mensajes disponibles directamente en la interfaz OLE **IStorage** , es decir, con el identificador de interfaz IID_IStorage. El acceso a **IStorage** es compatible para permitir que un documento de Microsoft Word se coloque en datos adjuntos sin convertirlos a o desde la interfaz **IStream** OLE. Sin embargo, es posible que **IMessage** no se comporte de forma predecible si **OpenIMsgOnIStg** pasa un puntero **IStorage** a los datos adjuntos y, a continuación, los objetos se sueltan en el orden equivocado. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Archivo. cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI usa el método **OpenIMsgOnIStg** para abrir una interfaz IMessage en la parte superior del. MSG para que el archivo se pueda manipular con MAPI.  <br/> |
   
## <a name="see-also"></a>Vea también

- [MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

