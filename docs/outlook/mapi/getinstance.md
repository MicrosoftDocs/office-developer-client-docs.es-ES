---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816927"
---
# <a name="getinstance"></a>GetInstance

  
  
**Hace referencia a**: Outlook 
  
Copia un valor dentro de una propiedad multivalor a una propiedad de un solo valor del mismo tipo. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIUTIL. H  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Parámetros

 _pvalMv_
  
> [entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definir una propiedad multivalor. 
    
 _pvalSv_
  
> [entrada] Puntero a una propiedad de un solo valor para recibir datos. 
    
 _uliInst_
  
> [entrada] El número de instancia, que es, el elemento de la matriz, del valor que se copió desde la estructura indicada por el parámetro _pvalMv_ . 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Si el valor que se copia es demasiado grande para la memoria asignada, la función **GetInstance** sólo copia punteros en lugar de asignar memoria nueva. 
  

