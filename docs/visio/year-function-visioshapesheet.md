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
description: Devuelve un entero que representa el año gregoriano en fecha y hora o expresión, con formato según el estilo de fecha corta establecido por la configuración actual de región e idioma del sistema.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420713"
---
# <a name="year-function-visioshapesheet"></a>Función YEAR (VisioShapeSheet)

Devuelve un entero que representa el  año gregoriano en fecha y hora o expresión _,_ con formato según el estilo de fecha corta establecido por la configuración actual de región e idioma del sistema.
  
## <a name="syntax"></a>Sintaxis

YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**Varía** <br/> |Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Numérico** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Se descarta el componente de _hora en la fecha y_ hora o la expresión.  
  
No se realiza redondeo. Si  _falta fecha y_ hora o no se puede interpretar como una fecha u hora válidas, YEAR devuelve un error. 
  
La función YEAR también acepta un  valor numérico único para la expresión donde la parte entera del resultado representa el número de días desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

YEAR("10/27/2007 13:45:24")
  
Devuelve 2007.
  
## <a name="example-2"></a>Ejemplo 2

YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)
  
Devuelve 2007.
  
## <a name="example-3"></a>Ejemplo 3

YEAR(35580.6337)
  
Devuelve 1997.
  

