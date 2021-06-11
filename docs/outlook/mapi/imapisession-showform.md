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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412530"
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
  
> [in] Identificador de la ventana primaria del formulario.
    
 _lpMsgStore_
  
> [in] Puntero al almacén de mensajes que contiene la carpeta a la que apunta el _parámetro lpParentFolder._ 
    
 _lpParentFolder_
  
> [in] Puntero a la carpeta en la que se creó el mensaje asociado al parámetro _ulMessageToken._ 
    
 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al mensaje que se muestra en el formulario. El  _parámetro lpInterface_ debe ser NULL o IID_IMessage. Si se pasa NULL, se usa la [interfaz estándar, IMessage.](imessageimapiprop.md) 
    
 _ulMessageToken_
  
> [in] Token asociado al mensaje que se va a mostrar en el formulario. El  _parámetro ulMessageToken_ debe establecerse en el contenido del parámetro  _lpulMessageToken_ de la llamada anterior a [IMAPISession::P repareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Reservado; debe ser NULL. 
    
 _ulFlags_
  
> [in] Máscara de bits de marcas que controla cómo y si se guarda el mensaje. Se pueden establecer las siguientes marcas:
    
MAPI_NEW_MESSAGE 
  
> El mensaje nunca se ha guardado (es decir, nunca se ha llamado a su [método IMAPIProp::SaveChanges).](imapiprop-savechanges.md) 
    
MAPI_POST_MESSAGE 
  
> El mensaje debe guardarse en su carpeta primaria. El mensaje no se procesa para el envío, sino que se publica en la carpeta en su lugar. Si no se establece esta marca, el mensaje se copia en la Bandeja de salida y se procesa para su envío. 
    
 _ulMessageStatus_
  
> [in] Máscara de bits de marcas copiadas de la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje asociado con el token en el _parámetro ulMessageToken._ Las marcas proporcionan información sobre el estado del mensaje. 
    
 _ulMessageFlags_
  
> [in] Máscara de bits de marcas copiadas de la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje asociado con el token en el _parámetro ulMessageToken._ Estas marcas proporcionan más información sobre el estado del mensaje. 
    
 _ulAccess_
  
> [in] Marca que indica el nivel de permisos del mensaje que se muestra en el formulario. Esta información se copia de la **propiedad PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) del mensaje asociado con el token en el _parámetro ulMessageToken._ 
    
 _lpszMessageClass_
  
> [in] Puntero a la clase de mensaje del mensaje que se muestra en el formulario, copiado de la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje asociado con el token en el _parámetro ulMessageToken._ 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se ha mostrado correctamente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el **botón Cancelar** de un cuadro de diálogo. 
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::ShowForm** muestra un formulario de mensaje preparado por el método **IMAPISession::P repareForm.** 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Solo debe tener una sola referencia al mensaje pasado en el parámetro _lpMessage_ del método **PrepareForm.** 
  
Tenga en cuenta que las implementaciones de formulario pueden devolver valores de error distintos de los documentados por MAPI. Si puede usar estos valores de error para realizar una determinación más precisa de la condición de error, haga lo mismo. De lo contrario, controla estos errores como controlaría MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa el **método IMAPISession::ShowForm,** junto con el método **PrepareForm,** para mostrar un mensaje en un formulario modal.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

