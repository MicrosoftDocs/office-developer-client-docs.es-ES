---
title: Función MONTH (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Devuelve un entero entre 1 y 12 que representa un mes.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431977"
---
# <a name="month-function-visioshapesheet"></a>Función MONTH (VisioShapeSheet)

Devuelve un entero entre 1 y 12 que representa un mes.
  
## <a name="syntax"></a>Sintaxis

MONTH ("* * *DateTime* * *" | * * *expresión* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Se descarta el componente de hora de _fecha y_ hora o de _expresión_ . 
  
No se realiza redondeo. Si falta la cadena de entrada de datos o si ésta no se puede convertir en un valor válido, la función devuelve un error.
  
El formato del valor devuelto corresponde al estilo corto de fecha establecido en la configuración regional actual del sistema.
  
La función MONTH también acepta un único valor numérico en _expresión_ , en el que la parte entera del resultado representa el número de días transcurridos desde el 30 de diciembre de 1899. 
  
## <a name="example-1"></a>Ejemplo 1

MONTH("May 30, 1999 13:45:24")
  
Devuelve 5.
  
## <a name="example-2"></a>Ejemplo 2

MONTH(DATEVALUE("May 30, 1999")+7 ed.)
  
Devuelve 6.
  
## <a name="example-3"></a>Ejemplo 3

MES (35580.6337)
  
Devuelve 5.
  

