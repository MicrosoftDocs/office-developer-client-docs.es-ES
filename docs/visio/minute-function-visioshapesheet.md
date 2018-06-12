---
title: Función MINUTE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Devuelve un valor integer entre 0 y 59 que representa el componente de minutos de fecha y hora o expresión.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822659"
---
# <a name="minute-function-visioshapesheet"></a>Función MINUTE (VisioShapeSheet)

Devuelve un valor integer entre 0 y 59 que representa el componente de minutos de *fecha y hora* o *expresión* . 
  
## <a name="syntax"></a>Sintaxis

MINUTO (" *datetime* " |  *expresión*  [, *lcid* ]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

La fecha y _hora_ o de _expresión_ se descarta. 
  
No se realiza redondeo. Si falta _fecha y hora_ o si no se puede convertir en un resultado válido, la función devuelve un error. 
  
El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema.
  
La función MINUTE también acepta un único valor numérico en _expresión_ , donde la parte decimal representa la fracción de un día contada a partir de la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

MINUTE("7/7/1999 13:45:24")
  
Devuelve 45.
  
## <a name="example-2"></a>Ejemplo 2

MINUTE(TIMEVALUE("25 Ene., 1999 12:07:45")+6 em.)
  
Devuelve 13.
  
## <a name="example-3"></a>Ejemplo 3

MINUTE(0.575)
  
Devuelve 48.
  

