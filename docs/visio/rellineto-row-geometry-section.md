---
title: Fila RelLineTo (Sección de geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contiene las coordenadas x -e y del vértice final de un segmento de línea recta con relación al ancho y alto de una forma.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437165"
---
# <a name="rellineto-row-geometry-section"></a>Fila RelLineTo (Sección de geometría)

Contiene  *las coordenadas x*  -e  *y*  del vértice final de un segmento de línea recta con relación al ancho y alto de una forma. 
  
> [!NOTE]
> Una **fila RelLineTo** solo se puede conservar en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelLineTo** se convierte en una [fila LineTo.](lineto-row-geometry-section.md) 
  
Una **fila RelLineTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada  *x*  del vértice final de un segmento de línea recta con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada  *y*  del vértice final de un segmento de línea recta con relación al alto de la forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores de **la fila RelLineTo** son equivalentes a los valores de una fila [LineTo](lineto-row-geometry-section.md) multiplicados por el ancho y alto de la forma. Por ejemplo: una fila **RelLineTo** en la que el valor de la celda **X** es "0" y el valor de la celda **Y** es "0,5" se puede reemplazar por la fila **LineTo,** donde el valor de la celda **X** es la fórmula "Width *0"* y la celda Y es la fórmula "Height 0.5". 
  

