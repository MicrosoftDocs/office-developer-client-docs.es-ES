---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Establece el valor de la propiedad de cuenta especificado.
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816187"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Establece el valor de la propiedad de cuenta especificado.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parámetros

_dwProp_
  
> [entrada] La etiqueta de propiedad de la propiedad de cuenta para establecer.
    
_pVar_
  
> [entrada] El valor de la propiedad especificada.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada al método fue correcta.  <br/> |
|E_INVALIDARG  <br/> |Se ha especificado una etiqueta de propiedad no válido.  <br/> |
   
## <a name="remarks"></a>Comentarios

Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) para guardar los cambios en el valor de las propiedades de cuenta. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

