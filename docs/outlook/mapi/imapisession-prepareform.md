---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817450"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Hace referencia a**: Outlook 
  
Crea un token numérico que usa el método [IMAPISession:: ShowForm](imapisession-showform.md) para tener acceso a un mensaje. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Parámetros

 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje. **Null** resultados satisfactorios en la interfaz estándar, o [IMessage](imessageimapiprop.md), que se usa. El parámetro _lpInterface_ debe ser **nulo** o IID_IMessage. 
    
 _lpMessage_
  
> [entrada] Un puntero al mensaje que se mostrará en el formulario.
    
 _lpulMessageToken_
  
> [out] Un puntero a un símbolo (token) de mensaje que se usa en el método **IMAPISession:: ShowForm** para tener acceso al mensaje que apunta _lpMessage_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La preparación del formulario fue correcta.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISession:: PrepareForm** crea un símbolo (token) de mensaje para el mensaje que apunta el parámetro _lpMessage_ y llama a método [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) del mensaje. Este token se pasa en el parámetro _ulMessageToken_ al **IMAPISession:: ShowForm**. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si la llamada a **PrepareForm** se realiza correctamente, publicará el mensaje que apunta _lpMessage_ antes de llamar a **ShowForm**llamando a su método [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . Error al liberar el mensaje antes de llamar a **ShowForm** puede provocar pérdidas de memoria. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa el método **IMAPISession:: PrepareForm** , junto con **IMAPISession:: ShowForm**, para mostrar un mensaje en un formulario modal.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

