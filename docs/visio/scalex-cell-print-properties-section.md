---
title: Celda ScaleX (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823105"
---
# <a name="scalex-cell-print-properties-section"></a>Celda ScaleX (sección Propiedades de impresión)

Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.
  
## <a name="remarks"></a>Comentarios

Este valor solo se usa cuando el valor de la celda OnPage es FALSE. Las celdas ScaleX y ScaleY siempre tienen el mismo valor, que corresponde al valor de la opción **Ajustar a** en la ficha **Configurar impresión** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ). 
  
Para obtener una referencia a la celda ScaleX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ScaleX  <br/> |
   
Para obtener una referencia desde un programa a la celda ScaleX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
|Índice de celda:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

