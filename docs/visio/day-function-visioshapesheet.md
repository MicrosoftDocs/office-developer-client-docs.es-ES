---
title: Función DAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Devuelve un entero entre 1 y 31, que representa el día y hora o de expresión. La función día usa el calendario gregoriano.
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821952"
---
# <a name="day-function-visioshapesheet"></a>Función DAY (VisioShapeSheet)

Devuelve un entero entre 1 y 31, que representa el día _y hora_ o de _expresión_. La función día usa el calendario gregoriano.
  
## <a name="syntax"></a>Sintaxis

DÍA ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

Se descarta cualquier componente de hora _y hora_ o de _expresión_ . 
  
No se realiza redondeo. Si falta _fecha y hora_ o si no se puede convertir en un resultado válido, la función devuelve un error. 
  
La función DAY también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

DAY("May 30, 1997 15:45:24")
  
Devuelve 30.
  
## <a name="example-2"></a>Ejemplo 2

DAY(DATEVALUE("May 30, 1997")+7 ed.)
  
Devuelve 6.
  
## <a name="example-3"></a>Ejemplo 3

DAY(35580.6337)
  
Devuelve 30.
  

