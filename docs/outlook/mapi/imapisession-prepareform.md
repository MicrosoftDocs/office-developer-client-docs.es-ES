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
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393239"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
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

El método **IMAPISession:: PrepareForm** crea un símbolo (token) de mensaje para el mensaje que apunta el parámetro _lpMessage_ y llama a método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) del mensaje. Este token se pasa en el parámetro _ulMessageToken_ al **IMAPISession:: ShowForm**. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si la llamada a **PrepareForm** se realiza correctamente, publicará el mensaje que apunta _lpMessage_ antes de llamar a **ShowForm**llamando a su método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Error al liberar el mensaje antes de llamar a **ShowForm** puede provocar pérdidas de memoria. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa el método **IMAPISession:: PrepareForm** , junto con **IMAPISession:: ShowForm**, para mostrar un mensaje en un formulario modal.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

