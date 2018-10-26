---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1a1d11db538d9b5368d80962e44b9eab38b490d2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575654"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Quita un formulario en particular de un contenedor de formulario.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Parámetros

 _szMessageClass_
  
> [entrada] Una cadena que da nombre a la clase de mensaje del formulario que se quitará del contenedor del formulario. Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje que se pasa en el parámetro _szMessageClass_ no coincide con la clase de mensaje de cualquier formulario en el contenedor de formulario. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**File**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el método **IMAPIFormContainer::RemoveForm** para eliminar un formulario de un contenedor de formulario.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

