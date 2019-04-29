---
title: Fila RelCubBezTo (sección geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Contiene las coordenadas x e y del punto final de una curva Bézier cúbica en relación con el ancho y el alto de la forma, las coordenadas x e y del punto de control del principio del ancho y el alto de la forma relativa de la curva, y las coordenadas x-e y-de contr punto l del final del ancho y alto de la forma relativa de la curva.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430332"
---
# <a name="relcubbezto-row-geometry-section"></a>Fila RelCubBezTo (sección geometría)

Contiene las coordenadas *x* e ** y del punto final de una curva Bézier cúbica en relación con el ancho y el alto de la forma, las coordenadas *x* e y del punto de control del principio del ancho y el alto de la forma relativa de la curva. ** y las coordenadas *x* -e *y* -del punto de control del final del ancho y alto de la forma relativa de la curva. 
  
> [!NOTE]
> Una fila **RelCubBezTo** solo puede persistir en los formatos de archivo. vsdx,. vsdm,. vstx,. vstm,. vssx y. VSSM. Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelCubBezTo** se convierte en [](nurbsto-row-geometry-section.md) una fila NURBSTo. 
  
Una fila **RelCubBezTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada *x* del vértice del extremo de una curva cúbica de Bézier con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada *y* del vértice del extremo de una curva cúbica de Bézier con relación al alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordenada *x* del punto de control inicial de la curva con respecto al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor situado entre los vértices inicial y final del arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordenada *y* del punto de control inicial de una curva en relación con el alto de la forma.  <br/> |
|[CA](c-cell-geometry-section.md) <br/> |Coordenada *x* del punto de control final de la curva con respecto al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor situado entre el punto de control inicial y los vértices finales del arco.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Coordenada *y* del punto de control final de una curva en relación con el alto de la forma.  <br/> |
   

