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
  
Crea un nuevo archivo de datos adjuntos.
  
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
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al mensaje. Pasar resultados NULL en la interfaz estándar del mensaje o **IMessage**que se devuelve. 
    
 _ulFlags_
  
> a Máscara de máscara de marcadores que controla cómo se crean los datos adjuntos. Se puede establecer la siguiente marca:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **CreateAttach** se devuelva correctamente, posiblemente antes de que el cliente de llamada pueda obtener acceso total a los datos adjuntos. Si no se puede tener acceso a los datos adjuntos, realizar una llamada posterior al mismo puede dar lugar a un error. 
    
 _lpulAttachmentNum_
  
> contempla Puntero a un número de índice que identifica los datos adjuntos recién creados. Este número solo es válido cuando el mensaje está abierto y es la base de la propiedad **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de los datos adjuntos.
    
 _lppAttach_
  
> contempla Puntero a un puntero al objeto Attachment abierto.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Los datos adjuntos se crearon correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IMessage:: CreateAttach** crea nuevos datos adjuntos en un mensaje. Los nuevos datos adjuntos y las propiedades que se configuran para él no estarán disponibles hasta que un cliente haya llamado al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) del archivo y al método **IMAPIProp:: SaveChanges** del mensaje. 
  
El número de datos adjuntos a los que apunta _lpulAttachmentNum_ es único y válido únicamente en el contexto del mensaje. Es decir, dos datos adjuntos en dos mensajes diferentes pueden tener el mismo número, mientras que dos datos adjuntos en el mismo mensaje no pueden. 
  
## <a name="see-also"></a>Ver también



[IMessage: IMAPIProp](imessageimapiprop.md)

