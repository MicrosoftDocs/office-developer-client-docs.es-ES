---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417675"
---
# <a name="imessagecreateattach"></a>IMessage::CreateAttach

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un nuevo dato adjunto.
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al mensaje. Si se pasa NULL, se devuelve la interfaz estándar del mensaje o **IMessage.** 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo se crean los datos adjuntos. Se puede establecer la siguiente marca:
    
MAPI_DEFERRED_ERRORS 
  
> Permite **que CreateAttach** vuelva correctamente, posiblemente antes de que el cliente que realiza la llamada pueda acceder a los datos adjuntos. Si los datos adjuntos no son accesibles, realizar una llamada posterior a él puede provocar un error. 
    
 _lpulAttachmentNum_
  
> [salida] Puntero a un número de índice que identifica los datos adjuntos recién creados. Este número solo es válido cuando el mensaje está abierto y es la base para la propiedad PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
    
 _lppAttach_
  
> [salida] Puntero a un puntero al objeto de datos adjuntos abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se crearon correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMessage::CreateAttach** crea un nuevo dato adjunto en un mensaje. Los nuevos datos adjuntos y las propiedades que se establecen para él, no están disponibles hasta que un cliente haya llamado al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de los datos adjuntos y al método **IMAPIProp::SaveChanges del mensaje.** 
  
El número de datos adjuntos señalado por  _lpulAttachmentNum_ es único y válido solo en el contexto del mensaje. Es decir, dos datos adjuntos en dos mensajes diferentes pueden tener el mismo número, mientras que dos datos adjuntos del mismo mensaje no pueden. 
  
## <a name="see-also"></a>Vea también



[IMessage: IMAPIProp](imessageimapiprop.md)

