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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817464"
---
# <a name="imapisessionshowform"></a>IMAPISession:: ShowForm

  
  
**Se aplica a**: Outlook 
  
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

## <a name="parameters"></a>Sintaxis

 _ulUIParam_
  
> [entrada] Identificador de la ventana principal del formulario.
    
 _lpMsgStore_
  
> [entrada] Un puntero al almacén de mensajes que contiene la carpeta indicada por el parámetro _lpParentFolder_ . 
    
 _lpParentFolder_
  
> [entrada] Un puntero a la carpeta en la que se creó el mensaje asociado con el parámetro _ulMessageToken_ . 
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje que se muestra en el formulario. El parámetro _lpInterface_ debe ser NULL o IID_IMessage. Si se pasa NULL da como resultado la interfaz estándar, [IMessage](imessageimapiprop.md), que se usa. 
    
 _ulMessageToken_
  
> [entrada] El token que está asociado con el mensaje que se mostrará en el formulario. El parámetro _ulMessageToken_ debe establecerse en el contenido del parámetro _lpulMessageToken_ de la llamada anterior a [IMAPISession:: PrepareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [entrada] Reservado; debe ser NULL. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo y si el mensaje se guarda. Se pueden establecer los siguientes indicadores:
    
MAPI_NEW_MESSAGE 
  
> El mensaje no se ha guardado nunca (es decir, su método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) se ha llamado nunca). 
    
MAPI_POST_MESSAGE 
  
> El mensaje debe guardarse en su carpeta principal. El mensaje no se procesa para el envío, pero se registra en la carpeta en su lugar. Si no se establece este indicador, el mensaje se copia en la Bandeja de salida y se procesa para el envío. 
    
 _ulMessageStatus_
  
> [entrada] Una máscara de bits de indicadores que se copió desde la propiedad **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ . Los indicadores de proporcionan información sobre el estado del mensaje. 
    
 _ulMessageFlags_
  
> [entrada] Una máscara de bits de indicadores que se copió desde la propiedad **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ . Estos marcadores proporcionan más información sobre el estado del mensaje. 
    
 _ulAccess_
  
> [entrada] Marca que indica el nivel de permisos para el mensaje que se muestra en el formulario. Esta información se copia desde la propiedad **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ . 
    
 _lpszMessageClass_
  
> [entrada] Un puntero a la clase de mensaje del mensaje que se muestra en el formulario, que se copió desde la propiedad **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) del mensaje asociado con el símbolo (token) en el parámetro _ulMessageToken_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El formulario se muestra correctamente.
    
MAPI_E_USER_CANCEL 
  
> El usuario canceló la operación, normalmente haciendo clic en el botón **Cancelar** en un cuadro de diálogo. 
    
## <a name="remarks"></a>Notas

El método **IMAPISession:: ShowForm** muestra un formulario de mensaje que se ha preparado en el método **IMAPISession:: PrepareForm** . 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Debe tener sólo una sola referencia para el mensaje que se pasa en el **PrepareForm** parámetro del método _lpMessage_ . 
  
Tenga en cuenta que las implementaciones de formulario pueden devolver valores de error que no sean las documentadas por MAPI. Si puede usar estos valores de error para realizar una determinación más precisa de la condición de error, lo haga. De lo contrario, controlar estos errores se deben controlar MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa el método **IMAPISession:: ShowForm** , junto con el método **PrepareForm** , para mostrar un mensaje en un formulario modal.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession:: PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

