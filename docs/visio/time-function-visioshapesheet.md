---
title: Función TIME (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Devuelve la hora representada por hora, minuto y segundo.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281000"
---
# <a name="time-function-visioshapesheet"></a>Función TIME (VisioShapeSheet)

Devuelve la hora representada por _hora_, _minuto_y _segundo_.
  
## <a name="syntax"></a>Sintaxis

TIEMPO (* * *hora* * *, * * *minuto* * *, * * *segundo* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El componente de hora.  <br/> |
| _minute_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El componente de minuto.  <br/> |
| _second_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El componente de segundo.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numeric
  
## <a name="example-1"></a>Ejemplo 1

HORA (15, 30, 30)
  
Devuelve el valor que representa las 15:30:30.
  
## <a name="example-2"></a>Ejemplo 2

FORMAT (tiempo (15, 30, 30), "HH: mm")
  
Devuelve el valor que representa las 15:30.
  
## <a name="example-3"></a>Ejemplo 3

TIME(15,30,30) + 8 eh.
  
Devuelve el valor que representa las 23:30:30.
  

