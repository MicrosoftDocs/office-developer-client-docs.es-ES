---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564608"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos valores de propiedad con un operador relacional especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parámetros

_lpSPropValue1_
  
> [entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definir el primer valor de la propiedad para realizar una comparación. 
    
_ulRelOp_
  
> [entrada] El operador relacional para usar en la comparación. Para los valores permitidos, vea la estructura [SComparePropsRestriction](scomparepropsrestriction.md) . 
    
_lpSPropValue2_
  
> [entrada] Puntero a una estructura de **SPropValue** define el segundo valor de la propiedad para realizar una comparación. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Los valores de propiedad cumplen al objeto relation especificado. 
    
FALSE 
  
> Los valores de propiedad no cumplen con el objeto relation especificado.
    
## <a name="remarks"></a>Comentarios

El método de comparación depende de los tipos de propiedad especificados en las definiciones de la propiedad [SPropValue](spropvalue.md) . Las funciones **FPropCompareProp** y [FPropContainsProp](fpropcontainsprop.md) se pueden usar para preparar las restricciones para generar una tabla. 
  
El orden de comparación es _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Si no coinciden con los tipos de propiedad de los valores de propiedad que se va a comparar, la función **FPropCompareProp** devuelve FALSE. 
  

