---
title: CEILING (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Redondea un número de 0 (cero) a la siguiente instancia de múltiplo. Si no se especifica múltiplo, el número se redondea dirección contraria a 0 hasta el siguiente entero.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821709"
---
# <a name="ceiling-function"></a>Función CEILING

Redondea un número de 0 (cero) a la siguiente aparición de _varios_. Si no se especifica _múltiplo_ , el número se redondea dirección contraria a 0 hasta el siguiente entero. 
  
## <a name="syntax"></a>Sintaxis

CEILING (** *número* **, ** *varios* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Número** <br/> |El número que desea redondear.  <br/> |
| _varios_ <br/> |Obligatorio  <br/> |**Número** <br/> |Varios a redondear a.  <br/> |
   
## <a name="remarks"></a>Comentarios

 _Número_ y _varios_ deben tener el mismo signo o un #NUM! se devuelve el error. Si _número_ o _múltiplo_ no se puede convertir en un valor, #VALUE! se devuelve el error. Si el _número_ o el _múltiplo_ es 0, el resultado es 0. 
  
## <a name="example-1"></a>Ejemplo 1

CEILING(3.7)
  
Devuelve 4.
  
## <a name="example-2"></a>Ejemplo 2

CEILING(-3.7)
  
Devuelve -4.
  
## <a name="example-3"></a>Ejemplo 3

CEILING (3.7, 0,25)
  
Devuelve 3,75.
  

