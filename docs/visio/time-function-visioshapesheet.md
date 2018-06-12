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
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823421"
---
# <a name="time-function-visioshapesheet"></a>Función TIME (VisioShapeSheet)

Devuelve la hora representada por _hora_, _minuto_y _segundo_.
  
## <a name="syntax"></a>Sintaxis

TIEMPO (** *hora* **, ** *minuto* **, ** *segundo* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El componente de hora.  <br/> |
| _minute_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El componente de minuto.  <br/> |
| _second_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El componente de segundo.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numeric
  
## <a name="example-1"></a>Ejemplo 1

TIME(15,30,30)
  
Devuelve el valor que representa las 15:30:30.
  
## <a name="example-2"></a>Ejemplo 2

FORMAT(TIME(15,30,30),"HH:mm")
  
Devuelve el valor que representa las 15:30.
  
## <a name="example-3"></a>Ejemplo 3

TIME(15,30,30) + 8 eh.
  
Devuelve el valor que representa las 23:30:30.
  

