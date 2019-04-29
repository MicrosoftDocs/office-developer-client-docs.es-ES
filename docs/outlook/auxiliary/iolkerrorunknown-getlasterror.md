---
title: IOlkErrorUnknownGetLastError
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f332de3-470d-9bc2-0c65-684bb58bcd7a
description: Obtiene una cadena de mensaje para el error especificado.
ms.openlocfilehash: 4d2aa3a7513687484988921734eb4c0e6f91226b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431704"
---
# <a name="iolkerrorunknowngetlasterror"></a>IOlkErrorUnknown::GetLastError

Obtiene una cadena de mensaje para el error especificado. 
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkErrorUnknown](iolkerrorunknown.md).
  
```cpp
HRESULT IOlkErrorUnknown::GetLastError(  
    HRESULT hr, 
    LPWSTR *ppwszError 
); 

```

## <a name="parameters"></a>Parameters

_Departamento_
  
> a Código de error que se va a buscar.
    
_ppwszError_
  
> contempla Mensaje de error que corresponde a *HR* . 
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_INVALIDARG  <br/> |Uno o más argumentos no son válidos.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

