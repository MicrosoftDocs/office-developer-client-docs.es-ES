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
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360315"
---
# <a name="datevalue-function-visioshapesheet"></a>Función DATEVALUE (VisioShapeSheet)

Devuelve el valor de fecha representado por  _datetime_ o  _expresión_.
  
## <a name="syntax"></a>Sintaxis

DATEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Datetime
  
## <a name="remarks"></a>Comentarios

Se descarta cualquier componente de *hora en fecha y* hora o expresión.  
  
Si  *falta fecha*  y hora o no se puede convertir en un resultado válido, DATEVALUE devuelve un #VALUE! error. 
  
El valor devuelto se muestra utilizando el estilo corto de fecha establecido en la configuración regional actual del sistema. 
  
La función DATEVALUE también acepta un  valor numérico único para la expresión donde la parte entera del resultado representa los días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

DATEVALUE(NOW( ))+5 ed.
  
Devuelve la fecha que será dentro de cinco días.
  
## <a name="example-2"></a>Ejemplo 2

DATEVALUE("19/7/1995 12:30")
  
Devuelve la fecha.
  
## <a name="example-3"></a>Ejemplo 3

DATEVALUE("Mayo 33, 1997")
  
Devuelve el error #VALUE!
  
## <a name="example-4"></a>Ejemplo 4

DATEVALUE(35580.6337)
  
Devuelve 30/5/1997.
  

