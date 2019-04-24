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
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328073"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Compara dos valores de propiedad mediante un operador relacional especificado. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parameters

_lpSPropValue1_
  
> a Puntero a una estructura [SPropValue](spropvalue.md) que define el primer valor de propiedad para la comparación. 
    
_ulRelOp_
  
> a Operador relacional que se va a usar en la comparación. Para los valores permitidos, vea la estructura [SComparePropsRestriction](scomparepropsrestriction.md) . 
    
_lpSPropValue2_
  
> a Puntero a una estructura **SPropValue** que define el segundo valor de la propiedad para la comparación. 
    
## <a name="return-value"></a>Valor devuelto

TRUE 
  
> Los valores de propiedad satisfacen la relación especificada. 
    
FALSE 
  
> Los valores de la propiedad no satisfacen la relación especificada.
    
## <a name="remarks"></a>Comentarios

El método de comparación depende de los tipos de propiedad especificados en las definiciones de propiedad [SPropValue](spropvalue.md) . Las funciones **FPropCompareProp** y [FPropContainsProp](fpropcontainsprop.md) se pueden usar para preparar restricciones para la generación de una tabla. 
  
El orden de comparación es _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Si los tipos de propiedad de los valores de propiedad que se van a comparar no coinciden, la función **FPropCompareProp** devuelve false. 
  

