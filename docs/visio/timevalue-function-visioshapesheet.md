---
title: TIMEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Devuelve el valor de hora representado por la fecha y hora o expresión, basado en la región del sistema y de idioma configuración.
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823407"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE Function (VisioShapeSheet)

Devuelve el valor de hora representado por la _fecha y hora_ o de _expresión_, se basa en idioma y región del sistema configuración.
  
## <a name="syntax"></a>Sintaxis

TIMEVALUE ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Varies** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.
  <br/> |
   
## <a name="remarks"></a>Observaciones

Se descarta cualquier componente de fecha _y hora_ o de _expresión_ . 
  
Si falta _fecha y hora_ o si no se puede convertir en un resultado válido, esta función devuelve #VALUE! error. 
  
La función TIMEVALUE también acepta un único valor numérico en _expresión_ , donde la parte decimal del resultado representa la fracción de un día contada a partir de la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

TIMEVALUE("6:00 a.m.")
  
Devuelve el valor que representa las 6:30 a. m.
  
## <a name="example-2"></a>Ejemplo 2

TIMEVALUE("14:30")+4 eh.+30 em.
  
Devuelve el valor que representa las 19:00:00.
  
## <a name="example-3"></a>Ejemplo 3

TIMEVALUE("11 a.m., 1 de julio de 1997")
  
Devuelve el valor que representa las 11:00 a. m.
  
## <a name="example-4"></a>Ejemplo 4

TIMEVALUE(0.6337)
  
Devuelve el valor que representa las 15:12:32.
  
## <a name="example-5"></a>Ejemplo 5

TIMEVALUE("7:89")
  
Devuelve el error #VALUE!
  

