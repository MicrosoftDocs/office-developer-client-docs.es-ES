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
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432201"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Quita un formulario determinado de un contenedor de formulario.
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>Parameters

 _szMessageClass_
  
> [in] Cadena que nombra la clase de mensaje del formulario que se va a quitar del contenedor del formulario. Los nombres de clase de mensaje siempre son cadenas ANSI, nunca Unicode.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
MAPI_E_NOT_FOUND 
  
> La clase de mensaje pasada en  _el parámetro szMessageClass_ no coincide con la clase de mensaje de ningún formulario del contenedor del formulario. 
    
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa el **método IMAPIFormContainer::RemoveForm** para eliminar un formulario de un contenedor de formularios.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

