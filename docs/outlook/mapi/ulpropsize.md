---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: bc00270b167c9f7317fa466d790d5020d961676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820905"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Se aplica a**: Outlook 
  
Devuelve el tamaño de un valor de propiedad único. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Sintaxis

 _lpSPropValue_
  
> [entrada] Puntero a una estructura de [SPropValue](spropvalue.md) definición de la propiedad que se va a medir. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores. 
    
MAPI_E_CALL_FAILED 
  
> Un error de origen desconocido o inesperado no puede completar la operación.
    
## <a name="remarks"></a>Notas

La función **UlPropSize** devuelve el tamaño, en bytes, del valor de propiedad para la propiedad especificada. No tiene en cuenta el tamaño del resto de la estructura **SPropValue** . 
  

