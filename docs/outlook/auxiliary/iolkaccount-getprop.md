---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtiene el valor de la propiedad de cuenta especificada.
ms.openlocfilehash: d24df8cfa9d54bee4614c1f31e12268748b8c986
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433741"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Obtiene el valor de la propiedad de cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameters

_dwProp_
  
> [in] Etiqueta de propiedad de la propiedad account que se debe obtener.
    
_pVar_
  
> [salida] Valor de la propiedad especificada.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |La propiedad no se encuentra para la cuenta determinada.  <br/> |
|E_INVALIDARG  <br/> |Se ha especificado una etiqueta de propiedad no válida.  <br/> |
   
## <a name="remarks"></a>Comentarios

Después de que este método devuelva, si el valor de la propiedad account es un tipo binario o de cadena, debe liberar  *pVar*  mediante [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

