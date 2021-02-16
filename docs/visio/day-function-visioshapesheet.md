---
title: Función DAY (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Devuelve un entero, de 1 a 31, que representa el día en la fecha y hora o expresión. La función DAY usa el calendario gregoriano.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360301"
---
# <a name="day-function-visioshapesheet"></a>Función DAY (VisioShapeSheet)

Devuelve un entero, de 1 a 31, que representa el día en  _fecha y hora_ o  _expresión_. La función DAY usa el calendario gregoriano.
  
## <a name="syntax"></a>Sintaxis

DAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Se descarta cualquier componente de _hora en fecha y_ hora o expresión.  
  
No se realiza redondeo. Si  _falta fecha y_ hora o no se puede convertir en un resultado válido, la función devuelve un error. 
  
La función DAY también acepta un  valor numérico único para la expresión donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

DAY("May 30, 1997 15:45:24")
  
Devuelve 30.
  
## <a name="example-2"></a>Ejemplo 2

DAY(DATEVALUE("May 30, 1997")+7 ed.)
  
Devuelve 6.
  
## <a name="example-3"></a>Ejemplo 3

DAY(35580.6337)
  
Devuelve 30.
  

