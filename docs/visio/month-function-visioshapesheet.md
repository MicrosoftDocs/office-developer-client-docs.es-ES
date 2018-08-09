---
title: MONTH Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Devuelve un número entero de 1 a 12 que representa un mes.
ms.openlocfilehash: e17803a153b4aadec34aa751da7efa077963bba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822662"
---
# <a name="month-function-visioshapesheet"></a>MONTH Function (VisioShapeSheet)

Devuelve un número entero de 1 a 12 que representa un mes.
  
## <a name="syntax"></a>Sintaxis

MONTH ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Número** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

El tiempo de _fecha y hora_ o de _expresión_ se descarta. 
  
No se realiza redondeo. Si falta la cadena de entrada de datos o si ésta no se puede convertir en un valor válido, la función devuelve un error.
  
El formato del valor devuelto corresponde al estilo corto de fecha establecido en la configuración regional actual del sistema.
  
La función MONTH también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

MONTH("May 30, 1999 13:45:24")
  
Devuelve 5.
  
## <a name="example-2"></a>Ejemplo 2

MONTH(DATEVALUE("May 30, 1999")+7 ed.)
  
Devuelve 6.
  
## <a name="example-3"></a>Ejemplo 3

MONTH(35580.6337)
  
Devuelve 5.
  

