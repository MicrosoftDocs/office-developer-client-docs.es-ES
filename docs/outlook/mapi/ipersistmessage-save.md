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
ms.openlocfilehash: 222d8257a802739ee8e513a0ea95a13f4b99322e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817867"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Hace referencia a**: Outlook 
  
Guarda un formulario revisado el mensaje desde la que se ha cargado o creado.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Parámetros

 _pMessage_
  
> [entrada] Un puntero al mensaje.
    
 _fSameAsLoad_
  
> [entrada] TRUE para indicar que el mensaje que apunta por _pMessage_ es el mensaje desde la que el formulario se ha cargado o creado; en caso contrario, es FALSE. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se ha guardado correctamente.
    
## <a name="remarks"></a>Comentarios

Visores de formulario llamar al método **IPersistMessage::Save** para guardar un formulario revisado en el mensaje desde la que se ha cargado o creado. 
  
 **Guardar** sólo se debe llamar cuando el formulario está en su estado [Normal](normal-state.md) . 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

No confirme los cambios guardados; es el autor de la llamada para confirmar los cambios. Nunca realice cambios en las propiedades que pertenecen al mensaje del formulario, excepto durante la llamada de **Guardar** . 
  
Si _fSameAsLoad_ está establecida en TRUE, puede guardar los cambios al mensaje existente del formulario. Si _fSameAsLoad_ está establecida en FALSE, debe copiar todas las propiedades del mensaje original en el mensaje que apunta _pMessage_ antes de realizar la operación de guardar. Utilice el método de [IMAPIProp::CopyTo](imapiprop-copyto.md) del mensaje original para copiar las propiedades. 
  
Cuando todas las propiedades se han copiado, especifique el estado de [NoScribble](noscribble-state.md) . Si no se producen errores, devuelve S_OK. De lo contrario, devolverá el error de la acción con errores. 
  
Si se llama a **Guardar** cuando el formulario está en cualquier estado que no sea Normal, devolver E_UNEXPECTED. 
  
Para obtener más información acerca de cómo guardar objetos de almacenamiento, consulte la documentación sobre los métodos [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>Vea también



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Estados de formulario](form-states.md)

