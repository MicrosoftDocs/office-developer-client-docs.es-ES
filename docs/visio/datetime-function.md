---
title: DATETIME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Devuelve el valor de fecha y hora representado por la fecha y hora o expresión.
ms.openlocfilehash: 001430acaf9fcb670e95157380e474e12b9728cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821939"
---
# <a name="datetime-function"></a>DATETIME (función)

Devuelve el valor de fecha y hora representado por la _fecha y hora_ o _expresión_.
  
## <a name="syntax"></a>Sintaxis

DATETIME ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Datetime
  
## <a name="remarks"></a>Observaciones

Si falta *fecha y hora* o si no se puede interpretar como una fecha u hora válidas, la función DATETIME devuelve #VALUE! error. 
  
El formato del valor devuelto corresponde al estilo corto de fecha y hora establecido en la configuración regional actual del sistema. 
  
La función DATETIME también acepta un único valor numérico en *expresión* , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899 y la parte decimal representa la fracción de un día contada a partir de la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

DATETIME("May 30, 1997")+5 ed.
  
Devuelve el valor que corresponde al 4/6/1997.
  
## <a name="example-2"></a>Ejemplo 2

FORMAT(DATETIME("5/20/1997 14:30:45"),"C")
  
Devuelve la cadena "martes, 20 de mayo de 1997, 2:30:45 p.m."
  
## <a name="example-3"></a>Ejemplo 3

DATETIME("1:30 p.m. 19 de julio")
  
Devuelve el valor que corresponde al 19/7/2001 1:30:00 p. m. (suponiendo que el año actual sea el 2001).
  
## <a name="example-4"></a>Ejemplo 4

DATETIME(35580.6337)
  
Devuelve el valor que corresponde al 30/5/1997 3:12:32 p. m.
  

