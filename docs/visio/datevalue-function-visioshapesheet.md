---
title: Función DATEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Devuelve el valor de fecha representado por fecha y hora o expresión.
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821937"
---
# <a name="datevalue-function-visioshapesheet"></a>Función DATEVALUE (VisioShapeSheet)

Devuelve el valor de fecha representado por _fecha y hora_ o _expresión_.
  
## <a name="syntax"></a>Sintaxis

DATEVALUE ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Datetime
  
## <a name="remarks"></a>Observaciones

Se descarta cualquier componente de hora *y hora* o de *expresión* . 
  
Si falta *fecha y hora* o si no se puede convertir en un resultado válido, esta función devuelve #VALUE! error. 
  
El valor devuelto se muestra utilizando el estilo corto de fecha establecido en la configuración regional actual del sistema. 
  
La función DATEVALUE también acepta un único valor numérico en *expresión* , donde la parte entera del resultado representa los días transcurridos desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

DATEVALUE(NOW( ))+5 ed.
  
Devuelve la fecha que será dentro de cinco días.
  
## <a name="example-2"></a>Ejemplo 2

DATEVALUE("7/19/1995 12:30")
  
Devuelve la fecha.
  
## <a name="example-3"></a>Ejemplo 3

DATEVALUE("Mayo 33, 1997")
  
Devuelve el error #VALUE!
  
## <a name="example-4"></a>Ejemplo 4

DATEVALUE(35580.6337)
  
Devuelve 30/5/1997.
  

