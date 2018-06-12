---
title: Celda PageScale (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm775
localization_priority: Normal
ms.assetid: e1da84b3-fd15-12b9-9342-0412e818b3b9
description: Determina el valor de la unidad de página en la escala de dibujo actual. La escala de dibujo de la página es la relación entre la unidad de la página mostrada en la celda PageScale y la unidad de dibujo que aparece en la celda DrawingScale.
ms.openlocfilehash: 0e1721ea667ad3bcd9f35880ab4e63bc90802c32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822755"
---
# <a name="pagescale-cell-page-properties-section"></a>Celda PageScale (Sección de propiedades de página)

Determina el valor de la unidad de página en la escala de dibujo actual. La escala de dibujo de la página es la relación entre la unidad de la página mostrada en la celda PageScale y la unidad de dibujo que aparece en la celda DrawingScale.
  
## <a name="remarks"></a>Observaciones

También puede establecer el valor de la celda PageScale en la ficha **Escala de dibujo** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ). El valor de la celda es el primero de los dos números en el cuadro **Escala predefinida** o **escala personalizada** , según la configuración de escala de dibujo seleccionada en **escala de dibujo**. Por ejemplo, si selecciona una escala arquitectónica para el dibujo, la escala de dibujo de la página es 3/32 "= 1'0". El valor de la celda PageScale es en 0,0938. (o 3/32") y el valor de la celda DrawingScale es 1 ft.
  
Para obtener una referencia a la celda PageScale por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PageScale  <br/> |
   
Para obtener una referencia a la celda PageScale por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPage** <br/> |
|Índice de celda:  <br/> |**visPageScale** <br/> |
   

