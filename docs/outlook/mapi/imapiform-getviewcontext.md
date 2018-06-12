---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817256"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Se aplica a**: Outlook 
  
Devuelve el contexto de la vista actual para el formulario. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Sintaxis

 _ppViewContext_
  
> [out] Un puntero a un puntero al contexto de la vista del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Contexto de la vista actual del formulario se devolvió correctamente. 
    
S_FALSE 
  
> No hay ningún contexto de vista para el formulario.
    
## <a name="remarks"></a>Notas

Visores de formulario, llame a **GetViewContext** para obtener un puntero para el contexto de vista establecido en una llamada anterior a [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Si no se ha realizado ninguna llamada anterior a **SetViewContext**, **GetViewContext** _ppViewContext_ se establece en NULL. 
  
## <a name="notes-to-implementers"></a>Notas para los implementadores

Copie el puntero de contexto de vista de su formulario en el puntero que se pasó por el Visor de formulario llamada en el parámetro _ppViewContext_ . Si el formulario no tiene un contexto de vista, establezca _ppViewContext_ en NULL. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utiliza el método **IMAPIForm::GetViewContext** para comprobar si un formulario tiene un contexto de vista.  <br/> |
   
## <a name="see-also"></a>Ver también



[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm: IUnknown](imapiformiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

