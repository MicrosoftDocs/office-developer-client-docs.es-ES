---
title: Fila RelCubBezTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contiene las coordenadas x - e y del extremo de una curva bézier cúbica en relación con el ancho y alto de la forma, las coordenadas x - e y del punto de control del principio del ancho y alto de la forma relativa de la curva, y las coordenadas x - e y del punto de control del final del ancho y alto de la forma relativa de la curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430332"
---
# <a name="relcubbezto-row-geometry-section"></a>Fila RelCubBezTo (sección Geometría)

Contiene las coordenadas  *x*  - e  *y*  del extremo de una curva bézier cúbica en relación con el ancho y alto de la forma, las coordenadas  *x*  -  *e y*  del punto de control del principio del ancho y alto de la forma relativa de la curva, y las coordenadas  *x*  - e y del  *punto*  de control del final del ancho y alto de la forma relativa de la curva. 
  
> [!NOTE]
> Una **fila RelCubBezTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo en los formatos Visio 2003-2010, la fila **RelCubBezTo** se convierte en una [fila NURBSTo.](nurbsto-row-geometry-section.md) 
  
Una **fila RelCubBezTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La coordenada  *x*  del vértice final de una curva bézier cúbica con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada  *y*  del vértice final de una curva bézier cúbica con relación al alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |La coordenada  *x*  del punto de control inicial de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor entre los vértices inicial y final del arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordenada  *y*  del punto de control inicial de una curva con relación al alto de la forma.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |La coordenada  *x*  del punto de control final de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor entre el punto de control inicial y los vértices finales del arco.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Coordenada  *y*  del punto de control final de una curva con relación al alto de la forma.  <br/> |
   

