---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309621"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Guarda un formulario revisado en el mensaje desde el que se ha cargado o creado.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Parameters

 _pMessage_
  
> a Un puntero al mensaje.
    
 _fSameAsLoad_
  
> a TRUE para indicar que el mensaje al que se apunta mediante _pMessage_ es el mensaje desde el que se ha cargado o creado el formulario; de lo contrario, FALSE. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se ha guardado correctamente.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman al método **IPersistMessage:: Save** para guardar de nuevo un formulario revisado en el mensaje desde el que se ha cargado o creado. 
  
 Solo se debe llamar a **Save** cuando el formulario está en su estado [normal](normal-state.md) . 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

No confirme los cambios guardados; el autor de la llamada debe confirmar los cambios. Nunca realice cambios en las propiedades que pertenecen al mensaje del formulario excepto durante la llamada a **Save** . 
  
Si _fSameAsLoad_ se establece en true, puede guardar los cambios realizados en el mensaje existente del formulario. Si _fSameAsLoad_ se establece en false, debe copiar todas las propiedades del mensaje original en el mensaje al que señala _pMessage_ antes de realizar la operación de guardado. Use el método [IMAPIProp:: CopyTo](imapiprop-copyto.md) del mensaje original para copiar las propiedades. 
  
Cuando se hayan copiado todas las propiedades, escriba el [](noscribble-state.md) estado noscribble. Si no se produce ningún error, devuelva S_OK. De lo contrario, devuelva el error de la acción fallida. 
  
Si se llama a **Save** cuando el formulario está en cualquier Estado que no sea normal, se devuelve E_UNEXPECTED. 
  
Para obtener más información acerca de cómo guardar objetos de almacenamiento, consulte la documentación de los métodos [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulario](form-states.md)

