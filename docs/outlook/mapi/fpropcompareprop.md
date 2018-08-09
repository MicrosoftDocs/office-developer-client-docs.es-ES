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
ms.openlocfilehash: 69bbed644a8173bf9291ca48a63960f693108318
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816870"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Hace referencia a**: Outlook 
  
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
  

