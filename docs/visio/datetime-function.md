---
title: DATETIME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Devuelve el valor de fecha y hora representado por datetime o expresión.
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360322"
---
# <a name="datetime-function"></a>Función DATETIME

Devuelve el valor de fecha y hora representado por  _datetime_ o  _expresión_.
  
## <a name="syntax"></a>Sintaxis

DATETIME(" ** *datetime* ** "| ** *expresión* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Datetime
  
## <a name="remarks"></a>Comentarios

Si  *falta datetime*  o no se puede interpretar como una fecha u hora válidas, DATETIME devuelve un #VALUE! error. 
  
El formato del valor devuelto corresponde al estilo corto de fecha y hora establecido en la configuración regional actual del sistema. 
  
La función DATETIME también acepta un  valor de número único para la expresión donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899 y la parte decimal representa la fracción de un día desde la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

DATETIME("May 30, 1997")+5 ed.
  
Devuelve el valor que corresponde al 4/6/1997.
  
## <a name="example-2"></a>Ejemplo 2

FORMAT(DATETIME("5/20/1997 14:30:45"),"C")
  
Devuelve la cadena "martes, 20 de mayo de 1997, 2:30:45 p.m."
  
## <a name="example-3"></a>Ejemplo 3

DATETIME("1:30 p.m. 19 de julio")
  
Devuelve el valor que corresponde al 19/7/2001 1:30:00 p. m. (suponiendo que el año actual sea el 2001).
  
## <a name="example-4"></a>Ejemplo 4

DATETIME(35580.6337)
  
Devuelve el valor que corresponde al 30/5/1997 3:12:32 p. m.
  

