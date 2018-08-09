---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: Obtiene el valor de la propiedad de cuenta especificado.
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816170"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

Obtiene el valor de la propiedad de cuenta especificado.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parámetros

_dwProp_
  
> [entrada] La etiqueta de propiedad de la propiedad cuenta que se va a obtener.
    
_pVar_
  
> [out] El valor de la propiedad especificada.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada ha sido correcta.  <br/> |
|E_ACCT_NOT_FOUND  <br/> |No se encontró la propiedad para la cuenta especificada.  <br/> |
|E_INVALIDARG  <br/> |Se ha especificado una etiqueta de propiedad no válido.  <br/> |
   
## <a name="remarks"></a>Comentarios

Después de que este método devuelve, si el valor de la propiedad de cuenta es un tipo de archivo binario o cadena, debe liberar *pVar* mediante [IOlkAccount::FreeMemory](iolkaccount-freememory.md).
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

