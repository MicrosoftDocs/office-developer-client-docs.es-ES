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
description: Devuelve un valor integer, de 1 a 7, que representa el día de la semana en fechaHora o expresión.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285248"
---
# <a name="weekday-function-visioshapesheet"></a>Función WEEKDAY (VisioShapeSheet)

Devuelve un valor integer, de 1 a 7, que representa el día de la semana en _fechaHora_ o _expresión_.
  
## <a name="syntax"></a>Sintaxis

WEEKDAY ("* * *DateTime* * *" | * * *expresión* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Diferencias** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numeric** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Se descarta el componente de hora de _fecha_ y hora o de _expresión_ . 
  
El resultado se corresponde con el lunes (1) y domingo (7). No se realiza redondeo. Si falta _fechaHora_ o no se puede interpretar como una fecha u hora válidas, la función devuelve un #VALUE! error. 
  
La función WEEKDAY también acepta un único valor numérico en _expresión_ , en el que la parte entera del resultado representa el número de días transcurridos desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

WEEKDAY("30 Mayo, 1999")
  
Devuelve 7.
  
## <a name="example-2"></a>Ejemplo 2

WEEKDAY(DATEVALUE("30 May., 1999")+2 ed.)
  
Devuelve 2.
  
## <a name="example-3"></a>Ejemplo 3

WEEKDAY (35880.6337)
  
Devuelve 4.
  

