---
title: Fila MoveTo (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Contiene las coordenadas x e y del primer vértice de una forma o representa las coordenadas x e y del primer vértice después de una interrupción en una ruta de acceso.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283861"
---
# <a name="moveto-row-geometry-section"></a>Fila MoveTo (Sección de Geometría)

Contiene las coordenadas *x* e ** y del primer vértice de una forma o representa las coordenadas *x* e y del primer vértice ** después de una interrupción en una ruta de acceso. 
  
Las **** filas moveTo contienen las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la **** fila MoveTo es la primera fila de la sección, la celda x representa la coordenada *x* del primer vértice de la forma. Si la **** fila MoveTo aparece entre dos filas, la celda x representa la coordenada *x* del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la **** fila MoveTo es la primera fila de la sección, la celda y representa la coordenada *Y* del primer vértice de la forma. Si la **** fila MoveTo aparece entre dos filas, la celda y representa la coordenada *Y* del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

La fila **moveTo** contiene las coordenadas *x* e ** y del primer vértice de la forma si la fila MoveTo **** es la primera fila de la sección. Normalmente, se trata del primer vértice que se colocó al dibujar la forma y no corresponde necesariamente con el punto inicial de una forma unidimensional (1D). 
  
Una sección Geometry debe comenzar con **RelMoveTo** o una fila **moveTo** , pero también puede usar las filas moveTo **** y **RelMoveTo** para representar un hueco en el trazado de la ruta de acceso de una forma. Sin embargo, cuando la trayectoria se utiliza para definir el límite de una zona rellena, esta interrupción se interpreta como segmento de línea recta. Para insertar dicha brecha, inserte una fila entre dos filas y cambie el tipo de fila a **moveTo**. Si la fila **moveTo** se encuentra entre dos filas, contiene las coordenadas *x* e ** y del primer vértice de la línea después de la interrupción de la ruta de acceso de la forma. 
  

