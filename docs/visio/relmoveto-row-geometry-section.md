---
title: Fila RelMoveTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Contiene las coordenadas x - e y del primer vértice de una forma o x - e y -coordenadas del primer vértice después de un salto en una ruta de acceso, en relación con el alto y el ancho de la forma.
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414203"
---
# <a name="relmoveto-row-geometry-section"></a>Fila RelMoveTo (sección Geometría)

Contiene las  *coordenadas x*  - e  *y*  del primer vértice de una forma o  *x*  - e  *y*  -coordenadas del primer vértice después de un salto en una ruta de acceso, en relación con el alto y el ancho de la forma. 
  
> [!NOTE]
> Una **fila RelMoveTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo en los formatos Visio 2003-2010, la fila **RelMoveTo** se convierte en una [fila MoveTo.](moveto-row-geometry-section.md) 
  
Una **fila RelMoveTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la **fila RelMoveTo** es la primera fila de la sección, la celda X representa la coordenada  *x*  del primer vértice de una forma con relación al ancho de la forma. Si la **fila RelMoveTo** aparece entre dos filas, la celda X representa la coordenada  *x*  del primer vértice después del salto en la ruta de acceso.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la **fila RelMoveTo** es la primera fila de la sección, la celda Y representa la coordenada  *y*  del primer vértice de una forma. Si la **fila RelMoveTo** aparece entre dos filas, la celda Y representa la coordenada  *y*  del primer vértice después del salto en la ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores de **la fila RelMoveTo** son equivalentes a los valores de una fila [MoveTo](moveto-row-geometry-section.md) que se multiplican por el ancho y el alto de la forma. Por ejemplo: una fila **RelMoveTo** donde el valor de la celda **X** es "0" y el valor de la celda Y es "0,5" podría reemplazarse con la fila **MoveTo** donde el valor de la celda **X** es la fórmula "Width *0"* y la celda **Y** es la fórmula "Height 0.5". 
  
La **fila RelMoveTo** contiene las coordenadas  *x*  - e  *y*  del primer vértice de la forma si la fila MoveTo es la primera fila de la sección. Normalmente, se trata del primer vértice que se colocó al dibujar la forma y no corresponde necesariamente con el punto inicial de una forma unidimensional (1D). 
  
Una **sección Geometry** debe comenzar por una fila **MoveTo** o **RelMoveTo,** pero también puede usar las filas **RelMoveTo** y **MoveTo** para representar un espacio en el trazado de una forma con relación al ancho y alto de la forma. Sin embargo, cuando la trayectoria se utiliza para definir el límite de una zona rellena, esta interrupción se interpreta como segmento de línea recta. Para insertar dicho espacio, inserte una fila entre dos filas y cambie el tipo de fila a **RelMoveTo**. Si la **fila RelMoveTo** está entre dos filas, contiene las coordenadas  *x*  - e  *y del*  primer vértice de la línea después del salto en la ruta de acceso de la forma. 
  

