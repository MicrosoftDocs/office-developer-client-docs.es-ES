---
title: Fila RelQuadBezTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contiene x - y y - coordenadas del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto y el x - e y-las coordenadas del punto de control del ancho y alto de la forma relativa de curva.
ms.openlocfilehash: 99796e85a857fd320598cb48993fc29bdfa4964d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822985"
---
# <a name="relquadbezto-row-geometry-section"></a>Fila RelQuadBezTo (sección Geometría)

Contiene *el *x* - y *y* - coordenadas del extremo de una curva Bézier cuadrática con respecto al ancho de la forma y el alto y el *x* - y* -las coordenadas del punto de control del ancho y alto de la forma relativa de curva. 
  
> [!NOTE]
> Una fila de **RelQuadBezTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelQuadBezTo** se convierte en una fila [NURBSTo](nurbsto-row-geometry-section.md) . 
  
Una fila de **RelQuadBezTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del vértice del extremo de una curva Bézier cuadrática con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del vértice del extremo de una curva Bézier cuadrática con relación al alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La *x* -coordenadas del punto de control de la curva con respecto al ancho de la forma; un punto en el arco. El punto de control es mejor encuentra acerca de la mitad de la distancia entre el principio y el vértice final del arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |La *y* -coordenadas del punto de control de la curva con relación al alto de la forma.  <br/> |
   

