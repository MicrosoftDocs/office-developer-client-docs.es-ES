---
title: Función TIMEVALUE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Devuelve el valor de hora representado por fecha y hora o expresión, en función de la configuración de región e idioma del sistema.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432327"
---
# <a name="timevalue-function-visioshapesheet"></a>Función TIMEVALUE (VisioShapeSheet)

Devuelve el valor de hora representado por  _datetime_ o  _expresión_, en función de la configuración de región e idioma del sistema.
  
## <a name="syntax"></a>Sintaxis

TIMEVALUE(" ** *datetime* ** "| ** *expresión* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Varía** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cualquier componente de fecha  _en datetime_ o  _expresión_ se descarta. 
  
Si  _falta datetime_ o no se puede convertir en un resultado válido, esta función devuelve un #VALUE! error. 
  
La función TIMEVALUE también acepta un  valor numérico único para la expresión donde la parte decimal del resultado representa la fracción de un día desde la medianoche. 
  
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
  

