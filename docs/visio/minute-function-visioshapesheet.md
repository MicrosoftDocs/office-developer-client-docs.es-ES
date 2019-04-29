---
title: Función MINUTE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Devuelve un valor Integer comprendido entre 0 y 59 que representa el componente de minutos de fechaHora o expresión.
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436569"
---
# <a name="minute-function-visioshapesheet"></a>Función MINUTE (VisioShapeSheet)

Devuelve un valor Integer comprendido entre 0 y 59 que representa el componente de minutos de *fechaHora* o *expresión* . 
  
## <a name="syntax"></a>Sintaxis

MINUTE (" *fecha y hora* " |  *expresión*  [, *LCID* ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _DateTime_ <br/> |Obligatorio  <br/> |**String** <br/> |Cualquier cadena que se pueda reconocer como una fecha y una hora, o una referencia a una celda que contenga una fecha y una hora.  <br/> |
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> | Cualquier expresión que produzca como resultado una fecha y una hora.  <br/> |
| _lcid_ <br/> |Opcional  <br/> |**Number** <br/> |Identificador regional que se usa para evaluar información de fecha y hora que no sea local. El identificador regional es un número que se describe en los archivos de encabezado del sistema.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Se descarta el componente de fecha de _DateTime_ y de _expresión_ . 
  
No se realiza redondeo. Si falta _fecha y hora_ o no se puede convertir en un resultado válido, la función devuelve un error. 
  
El formato del valor devuelto corresponde al estilo de hora establecido en la configuración regional actual del sistema.
  
La función MINUTE también acepta un único valor numérico en _expresión_ , en el que la parte decimal representa la fracción de un día a partir de la medianoche. 
  
## <a name="example-1"></a>Ejemplo 1

MINUTE ("7/7/1999 13:45:24")
  
Devuelve 45.
  
## <a name="example-2"></a>Ejemplo 2

MINUTE(TIMEVALUE("25 Ene., 1999 12:07:45")+6 em.)
  
Devuelve 13.
  
## <a name="example-3"></a>Ejemplo 3

MINUTO (0.575)
  
Devuelve 48.
  

