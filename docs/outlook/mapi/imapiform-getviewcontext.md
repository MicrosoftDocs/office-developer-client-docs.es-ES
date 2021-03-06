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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430906"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el contexto de vista actual del formulario. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameters

 _ppViewContext_
  
> [salida] Puntero a un puntero al contexto de vista del formulario.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El contexto de vista actual del formulario se ha devuelto correctamente. 
    
S_FALSE 
  
> No hay ningún contexto de vista para el formulario.
    
## <a name="remarks"></a>Comentarios

Los visores de formularios llaman a **GetViewContext** para obtener un puntero al contexto de vista establecido en una llamada anterior a [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Si no se ha realizado ninguna llamada previa a **SetViewContext,** **GetViewContext** establece  _ppViewContext_ en NULL. 
  
## <a name="notes-to-implementers"></a>Notas a los implementadores

Copie el puntero de contexto de vista del formulario en el puntero pasado por el visor de formularios de llamada en el _parámetro ppViewContext._ Si el formulario no tiene un contexto de vista, establezca  _ppViewContext_ en NULL. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa el **método IMAPIForm::GetViewContext** para comprobar si un formulario tiene un contexto de vista.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

