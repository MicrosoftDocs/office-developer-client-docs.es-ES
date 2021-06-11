---
title: Función SECOND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Devuelve un número entero, de 0 a 59, que representa el componente de segundos de datetime o expresión.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404879"
---
# <a name="second-function-visioshapesheet"></a>Función SECOND (VisioShapeSheet)

Devuelve un entero, de 0 a 59, que representa el componente de segundos de  _datetime_ o  _expresión_.
  
## <a name="syntax"></a>Sintaxis

SECOND(" ** *datetime* ** "| ** *expresión* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérico** <br/> |El identificador de configuración regional que se usará para evaluar una fecha y hora _no local._ El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

El componente date en  _datetime_ o  _expresión_ se descarta. 
  
No se realiza redondeo. Si  _falta datetime_ o no se puede convertir en un resultado válido, esta función devuelve un error. 
  
La función SECOND también acepta un  valor de número único para la expresión donde la parte decimal del resultado representa la fracción de un día desde la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

SECOND("05/30/1997 13:45:32")
  
Devuelve 32.
  
## <a name="example-2"></a>Ejemplo 2

SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)
  
Devuelve 52.
  
## <a name="example-3"></a>Ejemplo 3

SECOND(0.6337)
  
Devuelve 32.
  

