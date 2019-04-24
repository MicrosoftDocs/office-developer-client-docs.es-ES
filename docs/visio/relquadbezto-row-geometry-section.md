---
title: Fila RelQuadBezTo (sección geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Contiene las coordenadas x e y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma y las coordenadas x e y del punto de control del ancho y alto de la forma relativa de la curva.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319932"
---
# <a name="relquadbezto-row-geometry-section"></a>Fila RelQuadBezTo (sección geometría)

Contiene las coordenadas *x* e ** y del punto final de una curva Bézier cuadrática en relación con el ancho y el alto de la forma y las coordenadas *x* e ** y del punto de control del ancho y alto de la forma relativa de la curva. 
  
> [!NOTE]
> Una fila **RelQuadBezTo** solo puede persistir en los formatos de archivo. vsdx,. vsdm,. vstx,. vstm,. vssx y. VSSM. Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelQuadBezTo** se convierte en [](nurbsto-row-geometry-section.md) una fila NURBSTo. 
  
Una fila **RelQuadBezTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada *x* del vértice del extremo de una curva cuadrática de Bézier con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada *y* del vértice del extremo de una curva cuadrática de Bézier en relación con el alto de la forma.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Coordenada *x* del punto de control de la curva con relación al ancho de la forma; un punto en el arco. El punto de control se encuentra mejor cerca de la mitad de la distancia entre los vértices inicial y final del arco.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Coordenada *y* del punto de control de una curva en relación con el alto de la forma.  <br/> |
   

