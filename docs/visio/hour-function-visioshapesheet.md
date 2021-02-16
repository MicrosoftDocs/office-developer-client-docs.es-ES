---
title: Función HOUR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Devuelve un entero, de 0 a 23, que representa la hora del día de la fecha y hora o la expresión.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429638"
---
# <a name="hour-function-visioshapesheet"></a>Función HOUR (VisioShapeSheet)

Devuelve un entero, de 0 a 23, que representa la hora del día de  _la fecha y hora_ o la  _expresión_.
  
## <a name="syntax"></a>Sintaxis

HOUR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> | Una cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Varía** <br/> |Una expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> | Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Se descarta el componente de  *fecha y*  hora  *y la*  expresión. 
  
No se realiza redondeo. Si falta  *la fecha y*  hora o no se puede convertir en un resultado válido, la función devuelve un error. 
  
El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema. 
  
La función HOUR también acepta un  valor numérico único para la expresión donde la parte decimal del resultado representa la fracción de un día desde la medianoche. 
  
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

HOUR("30/5/1997")
  
Devuelve 0.
  

