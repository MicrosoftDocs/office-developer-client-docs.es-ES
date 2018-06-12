---
title: Fila de RelCubBezTo (sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contiene x - y y - las coordenadas del punto final de una curva de Bézier cúbica con relación al ancho de la forma y height, x - y y - las coordenadas del punto de control del principio de la x y el alto y el ancho de la forma relativa de curva - e y-coordenadas del control Elija l de la hora de finalización del ancho y alto de la forma relativa de curva.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822937"
---
# <a name="relcubbezto-row-geometry-section"></a>Fila de RelCubBezTo (sección de geometría)

Contiene *el *x* - y *y* - las coordenadas del punto final de una curva de Bézier cúbica con relación al ancho de la forma y height, *x* - y* -las coordenadas del punto de control del principio de la forma relativa de curva width y height, y la *x* e *y* -las coordenadas del punto de control de la hora de finalización del ancho y alto de la forma relativa de curva. 
  
> [!NOTE]
> Una fila de **RelCubBezTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelCubBezTo** se convierte en una fila [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Una fila de **RelCubBezTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del vértice del extremo de una curva de Bézier cúbica con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del vértice del extremo de una curva de Bézier cúbica con relación al alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La *x* -coordenada de la curva inicial del punto de control con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor ubicado entre el principio y el vértice final del arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La *y* -coordenada de una curva inicial del punto de control con relación al alto de la forma.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |La *x* -coordenada de la curva final del punto de control con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor ubicado entre los vértices de final y de punto de control de principio del arco.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |La *y* -coordenada de una curva final del punto de control con relación al alto de la forma.  <br/> |
   

