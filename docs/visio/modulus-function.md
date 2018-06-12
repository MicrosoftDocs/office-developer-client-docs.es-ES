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
description: Devuelve el resto (módulo) que se produce cuando se divide un número por un divisor.
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822661"
---
# <a name="modulus-function"></a>MODULUS (función)

Devuelve el resto (módulo) que se produce cuando se divide un número por un divisor.
  
## <a name="syntax"></a>Sintaxis

MODULUS (** *número* **, ** *divisor* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Número** <br/> |El dividendo.  <br/> |
| _divisor_ <br/> |Obligatorio  <br/> |**Número** <br/> |El divisor.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Observaciones

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
  

