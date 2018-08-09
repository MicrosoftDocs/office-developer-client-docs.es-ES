---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Devuelve un entero entre 0 y 23, que representa la hora del día de fecha y hora o expresión.
ms.openlocfilehash: 9cfe8c88a4a4d73be23b2ac230b0cfabc955c004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822293"
---
# <a name="hour-function-visioshapesheet"></a>HOUR Function (VisioShapeSheet)

Devuelve un entero entre 0 y 23, que representa la hora del día de _fecha y hora_ o _expresión_.
  
## <a name="syntax"></a>Sintaxis

HORA ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> | Una cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Varies** <br/> |Una expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> | Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
## <a name="remarks"></a>Observaciones

La fecha y *hora* o de *expresión* se descarta. 
  
No se realiza redondeo. Si la *fecha y hora* falta o no se puede convertir en un resultado válido, la función devuelve un error. 
  
El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema. 
  
La función HOUR también acepta un único valor numérico en *expresión* , donde la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

HOUR("15:45")
  
Devuelve 15.
  
## <a name="example-2"></a>Ejemplo 2

HOUR("Mayo 30, 1997 3:45:24 pm")
  
Devuelve 15.
  
## <a name="example-3"></a>Ejemplo 3

HOUR(0.5)
  
Devuelve 12.
  
## <a name="example-4"></a>Ejemplo 4

HOUR("5/30/1997")
  
Devuelve 0.
  

