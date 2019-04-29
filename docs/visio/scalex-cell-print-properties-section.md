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
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410213"
---
# <a name="scalex-cell-print-properties-section"></a>Celda ScaleX (sección de propiedades de impresión)

Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.
  
## <a name="remarks"></a>Comentarios

Este valor solo se usa cuando el valor de la celda OnPage es FALSE. Las celdas ScaleX y scaleY siempre tienen el mismo valor, que corresponde al valor de la opción **ajustar a** de la ficha **Configurar impresión** del cuadro de diálogo **Configurar página** (en la ficha **diseño** , haga clic en la flecha de **Configurar página** ). 
  
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
   

