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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335771"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea un token numérico que [el método IMAPISession::ShowForm](imapisession-showform.md) usa para obtener acceso a un mensaje. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para obtener acceso al mensaje. Si **se pasa null,** se usa la interfaz estándar o [IMessage.](imessageimapiprop.md) El  _parámetro lpInterface_ debe ser **null** o IID_IMessage. 
    
 _lpMessage_
  
> [in] Puntero al mensaje que se va a mostrar en el formulario.
    
 _lpulMessageToken_
  
> [salida] Puntero a un token de mensaje, que usa el método **IMAPISession::ShowForm** para tener acceso al mensaje señalado por  _lpMessage_.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La preparación del formulario se ha realizado correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISession::P repareForm** crea un token de mensaje para el mensaje señalado por el parámetro  _lpMessage_ y llama al método [IUnknown::AddRef del](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) mensaje. Este token se pasa en el  _parámetro ulMessageToken_ a **IMAPISession::ShowForm**. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Si la llamada a **PrepareForm** se realiza correctamente, libere el mensaje señalado por  _lpMessage_ llamando a su [método IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) antes de llamar **a ShowForm**. Si no se libera el mensaje antes de llamar a **ShowForm,** se pueden producir pérdidas de memoria. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa el método **IMAPISession::P repareForm,** junto con **IMAPISession::ShowForm**, para mostrar un mensaje en un formulario modal.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

