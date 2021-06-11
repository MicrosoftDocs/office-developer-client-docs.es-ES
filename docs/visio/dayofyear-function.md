---
title: DAYOFYEAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Devuelve un número entero, de 1 a 366, que representa el día secuencial del año en datetime o expresión. La función DAYOFYEAR usa el calendario gregoriano.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439454"
---
# <a name="dayofyear-function"></a>Función DAYOFYEAR

Devuelve un entero, de 1 a 366, que representa el día secuencial del año en  _datetime_ o  _expresión_. La función DAYOFYEAR usa el calendario gregoriano.
  
## <a name="syntax"></a>Sintaxis

DAYOFYEAR(" ** *datetime* ** "| ** *expresión* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> |Especifica el identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Cualquier componente de hora  _en datetime_ o  _expresión_ se descarta. 
  
El resultado corresponde a la fecha entre el 1 de enero y el 31 de diciembre. No se realiza ningún redondeo. Si  _falta datetime_ o no se puede interpretar como una fecha u hora válidas, la función devuelve un error. 
  
La función DAYOFYEAR también acepta un  valor de número único para la expresión donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

DAYOFYEAR("May 30, 1997 13:45:24")
  
Devuelve 150.
  
## <a name="example-2"></a>Ejemplo 2

DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)
  
Devuelve 157.
  
## <a name="example-3"></a>Ejemplo 3

DAYOFYEAR(35580.6337)
  
Devuelve 150.
  

