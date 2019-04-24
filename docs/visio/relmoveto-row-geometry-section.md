---
title: Fila RelMoveTo (sección geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Contiene las coordenadas x e y del primer vértice de una forma o las coordenadas x-e y del primer vértice después de una interrupción en una ruta de acceso, en relación con el alto y ancho de la forma.
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319925"
---
# <a name="relmoveto-row-geometry-section"></a>Fila RelMoveTo (sección geometría)

Contiene las coordenadas *x* e ** y del primer vértice de una forma o las coordenadas *x* -e *y* del primer vértice después de una interrupción en una ruta de acceso, en relación con el alto y ancho de la forma. 
  
> [!NOTE]
> Una fila **RelMoveTo** solo puede persistir en los formatos de archivo. vsdx,. vsdm,. vstx,. vstm,. vssx y. VSSM. Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelMoveTo** se convierte en [](moveto-row-geometry-section.md) una fila MoveTo. 
  
Una fila **RelMoveTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la fila **RelMoveTo** es la primera fila de la sección, la celda x representa la coordenada *x* del primer vértice de una forma en relación con el ancho de la forma. Si la fila **RelMoveTo** aparece entre dos filas, la celda x representa la coordenada *x* del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la fila **RelMoveTo** es la primera fila de la sección, la celda y representa la coordenada *Y* del primer vértice de una forma. Si la fila **RelMoveTo** aparece entre dos filas, la celda y representa la coordenada *Y* del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores de la fila **RelMoveTo** son equivalentes a los valores de una fila [moveTo](moveto-row-geometry-section.md) que se multiplican por el ancho y el alto de la forma. Por ejemplo: una fila **RelMoveTo** donde el valor de la celda **X** es "0" y el valor de la celda **Y** es "0,5" se puede reemplazar por una fila **moveTo** donde el valor de la celda **x** es la fórmula "width*0" y la celda **y** es la fórmula "altura*0,5". 
  
La fila **RelMoveTo** contiene las coordenadas *x* e ** y del primer vértice de la forma si la fila MoveTo es la primera fila de la sección. Normalmente, se trata del primer vértice que se colocó al dibujar la forma y no corresponde necesariamente con el punto inicial de una forma unidimensional (1D). 
  
Una sección **Geometry** debe comenzar con una fila **moveTo** o una fila **RelMoveTo** , pero también puede usar la fila **RelMoveTo** y **moveTo** para representar una brecha en el trazado de la ruta de una forma en relación con el ancho y el alto de la forma. Sin embargo, cuando la trayectoria se utiliza para definir el límite de una zona rellena, esta interrupción se interpreta como segmento de línea recta. Para insertar dicha brecha, inserte una fila entre dos filas y cambie el tipo de fila a **RelMoveTo**. Si la fila **RelMoveTo** está entre dos filas, contiene las coordenadas *x* e y ** del primer vértice de la línea después de la interrupción de la ruta de acceso de la forma. 
  

