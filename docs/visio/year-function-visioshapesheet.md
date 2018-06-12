---
title: Función YEAR (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Devuelve un valor de tipo integer que representa el año gregoriano de fecha y hora o expresión, con formato de acuerdo con el estilo corto de fecha establecido en configuración de idioma y región actual del sistema.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823600"
---
# <a name="year-function-visioshapesheet"></a>Función YEAR (VisioShapeSheet)

Devuelve un valor de tipo integer que representa el año gregoriano de _fecha y hora_ o _expresión_, con formato de acuerdo con el estilo corto de fecha establecido en configuración de idioma y región actual del sistema.
  
## <a name="syntax"></a>Sintaxis

AÑO ("** *datetime* **" | ** *expresión* ** [, ** *lcid* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _fecha y hora_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Varía** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérico** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Notas

Se descarta el componente de tiempo de _fecha y hora_ o de _expresión_ . 
  
No se realiza redondeo. Si falta _fecha y hora_ o si no se puede interpretar como una fecha u hora válidas, año devuelve un error. 
  
La función YEAR también acepta un único valor numérico en _expresión_ , donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

YEAR("10/27/2007 13:45:24")
  
Devuelve 2007.
  
## <a name="example-2"></a>Ejemplo 2

YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)
  
Devuelve 2007.
  
## <a name="example-3"></a>Ejemplo 3

YEAR(35580.6337)
  
Devuelve 1997.
  

