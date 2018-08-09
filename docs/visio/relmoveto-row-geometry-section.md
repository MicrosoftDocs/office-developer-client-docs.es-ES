---
title: Fila RelMoveTo (sección Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Contiene x - y y - las coordenadas del primer vértice de una forma o la x - e y-las coordenadas del primer vértice después de una interrupción de una ruta de acceso, en relación con el alto y el ancho de la forma.
ms.openlocfilehash: 77b3e731bfd1f35abe34ffbf3155b57133e56412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822952"
---
# <a name="relmoveto-row-geometry-section"></a>Fila RelMoveTo (sección Geometría)

Contiene *el *x* - y *y* - las coordenadas del primer vértice de una forma o la *x* - y* -las coordenadas del primer vértice después de una interrupción de una ruta de acceso, en relación con el alto y el ancho de la forma. 
  
> [!NOTE]
> Una fila de **RelMoveTo** sólo puede persistir en los formatos de archivo .vsdx, .vsdm, .vstx, .vstm, .vssx y .vssm. Cuando se guarda un archivo a los formatos de Visio 2003 2010, la fila de **RelMoveTo** se convierte en una fila [MoveTo](moveto-row-geometry-section.md) . 
  
Una fila de **RelMoveTo** contiene las celdas siguientes. 
  
|**Cell**|**Descripción**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Si la fila **RelMoveTo** es la primera fila en la sección, la celda X representa la *x* -coordenadas del primer vértice de una forma con relación al ancho de la forma. Si la fila **RelMoveTo** aparece entre dos filas, la celda X representa la *x* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Si la fila **RelMoveTo** es la primera fila en la sección, la celda Y representa la *y* -coordenadas del primer vértice de una forma. Si la fila **RelMoveTo** aparece entre dos filas, la celda Y representa la *y* -coordenadas del primer vértice después de la interrupción de la ruta de acceso.  <br/> |
   
## <a name="remarks"></a>Comentarios

Valores de la fila de **RelMoveTo** son equivalentes a los valores de una fila [MoveTo](moveto-row-geometry-section.md) que se multiplican por el ancho y el alto de la forma. Por ejemplo: una fila **RelMoveTo** donde el valor de la celda **X** es "0" y el valor de la celda **Y** es "0,5" podría reemplazarse con fila **MoveTo** donde el valor de la celda **X** es la fórmula "ancho*0" y la celda **Y** es la fórmula de "alto*0,5." 
  
La fila **RelMoveTo** contiene el *x* - e *y* -las coordenadas del primer vértice de la forma si la fila MoveTo es la primera fila en la sección. Suele ser el primer vértice que se colocó al dibujar la forma y no se corresponde necesariamente con el punto inicial de una forma 1-D. 
  
Una sección de **geometría** debe comenzar con un **MoveTo** o una fila de **RelMoveTo** , pero también puede utilizar la fila de **RelMoveTo** y la fila **MoveTo** para representar una interrupción en la trayectoria de una forma con relación al ancho y alto de la forma. Sin embargo, cuando se usa la ruta de acceso para definir el límite de una región rellena, esta interrupción se interpreta como un segmento de línea recta. Para insertar un espacio de este tipo, inserte una fila entre dos filas y cambie el tipo de fila a **RelMoveTo**. Si la fila **RelMoveTo** está entre dos filas, contiene el *x* - e *y* -las coordenadas del primer vértice de la línea después de la interrupción de la ruta de acceso de la forma. 
  

