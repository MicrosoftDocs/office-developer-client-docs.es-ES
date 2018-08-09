---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtiene una cadena de mensaje para el error especificado.
ms.openlocfilehash: 7b00392cdf65d1d4990f2231769e5126c9ae26dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816251"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Obtiene una cadena de mensaje para el error especificado. 
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkErrorUnknown](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Parámetros

_recursos humanos_
  
> [entrada] Código de error que se va a buscar.
    
_ppwszError_
  
> [out] El mensaje de error que corresponde a *recursos humanos* . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_INVALIDARG  <br/> |Uno o más argumentos no son válidos.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

