---
title: MODULUS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Devuelve el resto (módulo) que se produce cuando un número se divide por un divisor.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429274"
---
# <a name="modulus-function"></a>Función MODULUS

Devuelve el resto (módulo) que se produce cuando un número se divide por un divisor.
  
## <a name="syntax"></a>Sintaxis

MÓDULO (* * *número* * *, * * *Núm_divisor* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El dividendo.  <br/> |
| _visor_ <br/> |Obligatorio  <br/> |**Number** <br/> |El divisor.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

El resultado tiene el mismo signo que el divisor. Se devuelve el error #DIV/0! cuando el divisor vale 0. 
  
En casi todas las ocasiones es aconsejable utilizar la función MODULUS en lugar de la función MOD. 
  
## <a name="example-1"></a>Ejemplo 1

MODULUS(5, 1,4)
  
Devuelve 0,8.
  
## <a name="example-2"></a>Ejemplo 2

MODULUS(5, -1.4)
  
Devuelve -0,6.
  
## <a name="example-3"></a>Ejemplo 3

MODULUS(-5, 1,4)
  
Devuelve 0,6.
  
## <a name="example-4"></a>Ejemplo 4

MODULUS(-5, -1.4)
  
Devuelve -0,8.
  

