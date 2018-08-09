---
title: Fila RelLineTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contiene x - e y-coordenadas del vértice del extremo de un segmento de línea recta con relación al ancho y alto de una forma.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822941"
---
# <a name="rellineto-row-geometry-section"></a>Fila RelLineTo (sección Geometría)

Contiene *x* - e *y* -coordenadas del vértice del extremo de un segmento de línea recta con relación al ancho y alto de una forma. 
  
> [!NOTE]
> Una fila de **RelLineTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelLineTo** se convierte en una fila [LineTo](lineto-row-geometry-section.md) . 
  
Una fila de **RelLineTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |La *x* -coordenadas del vértice del extremo de un segmento de línea recta con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |La *y* -coordenadas del vértice del extremo de un segmento de línea recta con relación al alto de la forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Valores de la fila de **RelLineTo** son equivalentes a los valores de una fila [LineTo](lineto-row-geometry-section.md) que se multiplican por el ancho y el alto de la forma. Por ejemplo: una fila **RelLineTo** donde el valor de la celda **X** es "0" y el valor de la celda **Y** es "0,5" que se puede reemplazar con fila **LineTo** donde el valor de la celda **X** es la fórmula "ancho*0" y la celda **Y** es la fórmula de "alto*0,5." 
  

