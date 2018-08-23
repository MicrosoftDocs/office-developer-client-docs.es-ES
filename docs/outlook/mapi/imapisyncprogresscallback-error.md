---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594988"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información detallada que se muestra en el cuadro de diálogo de envío o recepción. Si se producen errores durante la sincronización, el proveedor de almacenamiento llama a esta función.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Parámetros

 **hResult**
  
> HRESULT del error o advertencia.
    
 **pwcszErrorStr**
  
> Un puntero a la cadena asociada con el error que se mostrará.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="see-also"></a>Recursos adicionales



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

