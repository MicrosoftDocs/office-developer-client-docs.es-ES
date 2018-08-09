---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Devuelve un entero entre 0 y 59, que representa el componente de segundos de fecha y hora o expresión.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823108"
---
# <a name="second-function-visioshapesheet"></a>SECOND Function (VisioShapeSheet)

Devuelve un entero entre 0 y 59, que representa el componente de segundos de _fecha y hora_ o _expresión_.
  
## <a name="syntax"></a>Sintaxis

SEGUNDO ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérico** <br/> |El identificador de configuración regional que se utiliza para evaluar una _fecha y hora_de no locales. El identificador de configuración regional es un número que se describen en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

La fecha _y hora_ o de _expresión_ se descarta. 
  
No se realiza redondeo. Si falta _fecha y hora_ o si no se puede convertir en un resultado válido, esta función devuelve un error. 
  
La función SECOND también acepta un único valor numérico en _expresión_ , donde la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

SECOND("05/30/1997 13:45:32")
  
Devuelve 32.
  
## <a name="example-2"></a>Ejemplo 2

SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)
  
Devuelve 52.
  
## <a name="example-3"></a>Ejemplo 3

SECOND(0.6337)
  
Devuelve 32.
  

