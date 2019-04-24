---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335668"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Muestra un formulario.
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de la ventana primaria del formulario.
    
 _lpMsgStore_
  
> a Un puntero al almacén de mensajes que contiene la carpeta a la que apunta el parámetro _lpParentFolder_ . 
    
 _lpParentFolder_
  
> a Un puntero a la carpeta en la que se creó el mensaje asociado con el parámetro _ulMessageToken_ . 
    
 _lpInterface_
  
> a Puntero al identificador de interfaz (IID) que representa la interfaz que se va a usar para obtener acceso al mensaje que se muestra en el formulario. El parámetro _lpInterface_ debe ser null o IID_IMessage. Pasar resultados NULL en la interfaz estándar, [IMessage](imessageimapiprop.md), que se está utilizando. 
    
 _ulMessageToken_
  
> a Token asociado al mensaje que se va a mostrar en el formulario. El parámetro _ulMessageToken_ debe establecerse en el contenido del parámetro _lpulMessageToken_ de la llamada anterior a [IMAPISession::P repareform](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> a Reserve debe ser NULL. 
    
 _ulFlags_
  
> a Una máscara de máscara de marcas que controla cómo y si se guarda el mensaje. Se pueden establecer los siguientes indicadores:
    
MAPI_NEW_MESSAGE 
  
> Nunca se ha guardado el mensaje (es decir, nunca se ha llamado al método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ). 
    
MAPI_POST_MESSAGE 
  
> El mensaje debe guardarse en su carpeta principal. El mensaje no se ha procesado para enviar, pero se ha publicado en la carpeta en su lugar. Si no se establece esta marca, el mensaje se copia en la bandeja de salida y se procesa para su envío. 
    
 _ulMessageStatus_
  
> a Una máscara de la máscara de los marcadores copiados de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ . Las marcas proporcionan información sobre el estado del mensaje. 
    
 _ulMessageFlags_
  
> a Una máscara de la máscara de los marcadores copiados de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ . Estas marcas proporcionan más información sobre el estado del mensaje. 
    
 _ulAccess_
  
> a Marca que indica el nivel de permisos del mensaje que se muestra en el formulario. Esta información se copia desde la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ . 
    
 _lpszMessageClass_
  
> a Un puntero a la clase de mensaje del mensaje que se muestra en el formulario, copiado de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje asociado con el token en el parámetro _ulMessageToken_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se mostró correctamente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: ShowForm** muestra un formulario de mensaje preparado por el método **IMAPISession::P repareform** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Solo debe haber una referencia al mensaje pasada en el parámetro _lpMessage_ del método **PrepareForm** . 
  
Tenga en cuenta que las implementaciones de formulario pueden devolver valores de error distintos a los documentados por MAPI. Si puede usar estos valores de error para realizar una determinación más precisa de la condición de error, hágalo. De lo contrario, controle estos errores tal y como lo haría con MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa el método **IMAPISession:: ShowForm** , junto con el método **PrepareForm** , para mostrar un mensaje en un formulario modal.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

