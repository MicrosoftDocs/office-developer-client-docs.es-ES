---
title: Fila RelLineTo (sección geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Contiene las coordenadas x e y del vértice del extremo de un segmento de línea recta con relación al ancho y el alto de la forma.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320072"
---
# <a name="rellineto-row-geometry-section"></a>Fila RelLineTo (sección geometría)

Contiene las coordenadas *x* e y del vértice del extremo de un segmento de línea recta con relación al ancho y el alto de la forma. ** 
  
> [!NOTE]
> Una fila **RelLineTo** solo puede persistir en los formatos de archivo. vsdx,. vsdm,. vstx,. vstm,. vssx y. VSSM. Cuando se guarda un archivo en los formatos de Visio 2003-2010, la fila **RelLineTo** se convierte en [](lineto-row-geometry-section.md) una fila lineTo. 
  
Una fila **RelLineTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Coordenada *x* del vértice del extremo de un segmento de línea recta con relación al ancho de la forma.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Coordenada *y* del vértice del extremo de un segmento de línea recta con relación al alto de la forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores de la fila **RelLineTo** son equivalentes a los valores de una fila [lineTo](lineto-row-geometry-section.md) que se multiplican por el ancho y el alto de la forma. Por ejemplo: una fila **RelLineTo** donde el valor de la celda **X** es "0" y el valor de la celda **Y** es "0,5" se puede reemplazar por una fila **lineTo** donde el valor de la celda **X** es la fórmula "width*0" y la celda **y** es la fórmula "altura*0,5". 
  

