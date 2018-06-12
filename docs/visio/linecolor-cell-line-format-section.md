---
title: Celda LineColor (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Determina el color de línea de la forma.
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822459"
---
# <a name="linecolor-cell-line-format-section"></a>Celda LineColor (Sección de formato de línea)

Determina el color de línea de la forma.
  
## <a name="remarks"></a>Observaciones

Para establecer el color de línea, escriba un número entre 0 y 23, que es un índice en una colección de colores de línea. Puede ver la colección de color de línea en el cuadro de diálogo **línea** (en la ficha **Inicio** , en el grupo **forma** , haga clic en **línea**, elija **grosor**y, a continuación, haga clic en **Más líneas**). También puede establecer el valor de LineColor en el cuadro de diálogo **línea** . 
  
Para especificar un color personalizado, utilice la función RGB o HSL. El valor de un color personalizado es su color RGB y RGB ( *r, g, b*), en lugar de un número, se mostrarán en la ventana ShapeSheet. Cuando se usa en operaciones numéricas, los colores personalizados tienen valores de 24 y superior. 
  
Puede establecer la transparencia del color de línea en la celda LineColorTrans.
  
Para obtener una referencia a la celda LineColor por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineColor  <br/> |
   
Para obtener una referencia a la celda LineColor por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLineColor** <br/> |
   

