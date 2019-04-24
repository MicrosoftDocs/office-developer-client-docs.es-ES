---
title: Función SECOND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Devuelve un valor integer, de 0 a 59, que representa el componente de segundos de fecha y hora o de expresión.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332791"
---
# <a name="second-function-visioshapesheet"></a>Función SECOND (VisioShapeSheet)

Devuelve un valor integer, de 0 a 59, que representa el componente de segundos de _fecha y hora_ o de _expresión_.
  
## <a name="syntax"></a>Sintaxis

SEGUNDO ("* * *DateTime* * *" | * * *expresión* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numeric** <br/> |El identificador de configuración regional que se va a usar para evaluar un _valor DateTime_que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Se descarta el componente de fecha de fecha _y hora_ o de _expresión_ . 
  
No se realiza redondeo. Si falta _fecha y hora_ o no se puede convertir en un resultado válido, la función devuelve un error. 
  
La segunda función también acepta un único valor numérico en _expresión_ , en el que la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

SEGUNDO ("05/30/1997 13:45:32")
  
Devuelve 32.
  
## <a name="example-2"></a>Ejemplo 2

SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)
  
Devuelve 52.
  
## <a name="example-3"></a>Ejemplo 3

SEGUNDO (0.6337)
  
Devuelve 32.
  

