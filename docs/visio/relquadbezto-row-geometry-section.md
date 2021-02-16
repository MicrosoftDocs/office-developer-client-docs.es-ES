---
title: Fila RelQuadBezTo (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contiene las coordenadas x - e y del extremo de una curva Bézier cuadrática en relación con el ancho y alto de la forma y las coordenadas x - e y del punto de control del ancho y alto relativos de la forma de curva.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423359"
---
# <a name="relquadbezto-row-geometry-section"></a>Fila RelQuadBezTo (Sección de geometría)

Contiene las coordenadas  *x*  - e  *y*  del extremo de una curva Bézier cuadrática en relación con el ancho y alto de la forma y las coordenadas  *x*  - e  *y*  del punto de control del ancho y alto relativos de la forma de curva. 
  
> [!NOTE]
> Una **fila RelQuadBezTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelQuadBezTo** se convierte en una fila [NURBSTo.](nurbsto-row-geometry-section.md) 
  
Una **fila RelQuadBezTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada  *x*  del vértice final de una curva Bézier cuadrática con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada  *y*  del vértice final de una curva Bézier cuadrática con relación al alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordenada  *x*  del punto de control de la curva con relación al ancho de la forma; un punto del arco. El punto de control se encuentra mejor a medio camino entre los vértices inicial y final del arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordenada  *y*  del punto de control de una curva con relación al alto de la forma.  <br/> |
   

