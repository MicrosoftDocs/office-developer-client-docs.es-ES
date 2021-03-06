---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: Establece el valor de la propiedad de cuenta especificada.
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431991"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

Establece el valor de la propiedad de cuenta especificada.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameters

_dwProp_
  
> [in] Etiqueta de propiedad de la propiedad account que se debe establecer.
    
_pVar_
  
> [in] Valor de la propiedad especificada.
    
## <a name="return-values"></a>Valores devueltos

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |La llamada al método se ha realizado correctamente.  <br/> |
|E_INVALIDARG  <br/> |Se especificó una etiqueta de propiedad no válida.  <br/> |
   
## <a name="remarks"></a>Comentarios

Use [IOlkAccount::SaveChanges](iolkaccount-savechanges.md) para guardar los cambios en el valor de las propiedades de la cuenta. 
  
## <a name="see-also"></a>Vea también

- [Constantes (API de administración de cuenta)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

