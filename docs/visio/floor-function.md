---
title: FLOOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Redondea un número hacia 0 (cero), al siguiente valor entero o a la siguiente instancia de múltiplo.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822151"
---
# <a name="floor-function"></a>Función FLOOR

Redondea un número hacia 0 (cero), hasta el siguiente entero o hasta la siguiente instancia de _múltiplo_.
  
## <a name="syntax"></a>Sintaxis

FLOOR (** *número* **, ** *varios* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Número** <br/> |El número que desea redondear.  <br/> |
| _varios_ <br/> |Obligatorio  <br/> |**Número** <br/> |El múltiple por el que redondear.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Comentarios

Si no se especifica _múltiplo_ , el número se redondea hacia 0 hasta el siguiente entero. 
  
 _Número_ y _varios_ deben tener el mismo signo o un #NUM! se devuelve el error. Si _número_ o _múltiplo_ no se puede convertir en un valor, #VALUE! se devuelve el error. Si el _número_ o el _múltiplo_ es 0, el resultado es 0. 
  
## <a name="example-1"></a>Ejemplo 1

FLOOR(3.7)
  
Devuelve 3.
  
## <a name="example-2"></a>Ejemplo 2

FLOOR(-3.7)
  
Devuelve -3.
  
## <a name="example-3"></a>Ejemplo 3

FLOOR (3.7, 0,5)
  
Devuelve 3,5.
  

