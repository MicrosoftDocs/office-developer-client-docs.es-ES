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
description: Contiene x - e y - las coordenadas del primer vértice de una forma o representa la x - e y-las coordenadas del primer vértice después de una interrupción de una ruta de acceso.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822663"
---
# <a name="moveto-row-geometry-section"></a>Fila MoveTo (Sección de Geometría)

Contiene el *x* - e *y* - las coordenadas del primer vértice de una forma o representa la *x* - e *y* -las coordenadas del primer vértice después de una interrupción de una ruta de acceso. 
  
Una fila **MoveTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la fila **MoveTo** es la primera fila en la sección, la celda X representa la *x* -coordenadas del primer vértice de una forma. Si la fila **MoveTo** aparece entre dos filas, la celda X representa la *x* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la fila **MoveTo** es la primera fila en la sección, la celda Y representa la *y* -coordenadas del primer vértice de una forma. Si la fila **MoveTo** aparece entre dos filas, la celda Y representa la *y* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Notas

La fila **MoveTo** contiene el *x* - e *y* -las coordenadas del primer vértice de la forma si la fila **MoveTo** es la primera fila en la sección. Suele ser el primer vértice que se colocó al dibujar la forma y no se corresponde necesariamente con el punto inicial de una forma 1-D. 
  
Una sección de geometría debe comenzar con un **RelMoveTo** o una fila **MoveTo** , pero también puede utilizar las filas **MoveTo** y **RelMoveTo** para representar una interrupción en la trayectoria de una forma. Sin embargo, cuando se usa la ruta de acceso para definir el límite de una región rellena, esta interrupción se interpreta como un segmento de línea recta. Para insertar un espacio de este tipo, inserte una fila entre dos filas y cambie el tipo de fila a **MoveTo**. Si la fila **MoveTo** está entre dos filas, contiene el *x* - e *y* -las coordenadas del primer vértice de la línea después de la interrupción de la ruta de acceso de la forma. 
  

