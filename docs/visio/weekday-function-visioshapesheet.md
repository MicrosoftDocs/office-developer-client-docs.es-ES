---
title: Función WEEKDAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Devuelve un entero entre 1 y 7, que representa el día de la semana de fecha y hora o expresión.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823543"
---
# <a name="weekday-function-visioshapesheet"></a>Función WEEKDAY (VisioShapeSheet)

Devuelve un entero entre 1 y 7, que representa el día de la semana de _fecha y hora_ o _expresión_.
  
## <a name="syntax"></a>Sintaxis

WEEKDAY ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Varía** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérico** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

Se descarta el componente de tiempo de _fecha y hora_ o de _expresión_ . 
  
El resultado corresponde al lunes (1) y el domingo (7). No se realiza redondeo. Si falta _fecha y hora_ o si no se puede interpretar como una fecha u hora válidas, la función devuelve #VALUE! error. 
  
La función WEEKDAY también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

WEEKDAY("30 Mayo, 1999")
  
Devuelve 7.
  
## <a name="example-2"></a>Ejemplo 2

WEEKDAY(DATEVALUE("30 May., 1999")+2 ed.)
  
Devuelve 2.
  
## <a name="example-3"></a>Ejemplo 3

WEEKDAY(35880.6337)
  
Devuelve 4.
  

