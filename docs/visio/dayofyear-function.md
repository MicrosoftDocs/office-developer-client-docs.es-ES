---
title: DAYOFYEAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Devuelve un entero entre 1 y 366, que representa el número de día del año de fecha y hora o expresión. La función DAYOFYEAR utiliza el calendario gregoriano.
ms.openlocfilehash: 2fd80a2554c268d276deaa524a9d98eebc6a48d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821962"
---
# <a name="dayofyear-function"></a>Función DAYOFYEAR

Devuelve un entero entre 1 y 366, que representa el número de día del año de _fecha y hora_ o _expresión_. La función DAYOFYEAR utiliza el calendario gregoriano.
  
## <a name="syntax"></a>Sintaxis

DAYOFYEAR ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

Se descarta cualquier componente de hora _y hora_ o de _expresión_ . 
  
El resultado corresponde a 1 de enero al 31 de diciembre. No se realiza redondeo. Si falta _fecha y hora_ o si no se puede interpretar como una fecha u hora válidas, la función devuelve un error. 
  
La función DAYOFYEAR también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

DAYOFYEAR("May 30, 1997 13:45:24")
  
Devuelve 150.
  
## <a name="example-2"></a>Ejemplo 2

DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)
  
Devuelve 157.
  
## <a name="example-3"></a>Ejemplo 3

DAYOFYEAR(35580.6337)
  
Devuelve 150.
  

