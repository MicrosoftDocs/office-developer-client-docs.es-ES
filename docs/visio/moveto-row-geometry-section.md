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
description: Contiene las coordenadas x - e y -del primer vértice de una forma, o representa las coordenadas x - e y del primer vértice después de un salto en una ruta de acceso.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429701"
---
# <a name="moveto-row-geometry-section"></a>Fila MoveTo (Sección de Geometría)

Contiene las  *coordenadas x*  -  *e y*  -del primer vértice de una forma, o representa las coordenadas  *x*  - e  *y del*  primer vértice después de un salto en una ruta de acceso. 
  
Una **fila MoveTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la **fila MoveTo** es la primera fila de la sección, la celda X representa la coordenada  *x*  del primer vértice de una forma. Si la **fila MoveTo** aparece entre dos filas, la celda X representa la coordenada  *x*  del primer vértice después del salto en la ruta de acceso.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la **fila MoveTo** es la primera fila de la sección, la celda Y representa la coordenada  *y*  del primer vértice de una forma. Si la **fila MoveTo** aparece entre dos filas, la celda Y representa la coordenada  *y*  del primer vértice después del salto en la ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

La **fila MoveTo** contiene las coordenadas  *x*  - e  *y*  del primer vértice de la forma si la fila **MoveTo** es la primera fila de la sección. Normalmente, se trata del primer vértice que se colocó al dibujar la forma y no corresponde necesariamente con el punto inicial de una forma unidimensional (1D). 
  
Una sección de geometría debe comenzar por una **fila RelMoveTo** o **MoveTo,** pero también puede usar las filas **MoveTo** y **RelMoveTo** para representar un espacio en el trazado de una forma. Sin embargo, cuando la trayectoria se utiliza para definir el límite de una zona rellena, esta interrupción se interpreta como segmento de línea recta. Para insertar dicho espacio, inserte una fila entre dos filas y cambie el tipo de fila a **MoveTo**. Si la **fila MoveTo** está entre dos filas, contiene las coordenadas  *x*  - e  *y*  del primer vértice de la línea después del salto en la ruta de acceso de la forma. 
  

