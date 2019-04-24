---
title: Celda ScaleY (Sección de propiedades de impresión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342731"
---
# <a name="scaley-cell-print-properties-section"></a>Celda ScaleY (sección de propiedades de impresión)

Especifica el porcentaje de ampliación de la página de dibujo en la página de la impresora.
  
## <a name="remarks"></a>Comentarios

Este valor solo se usa cuando el valor de la celda OnPage es FALSE. Las celdas ScaleX y scaleY siempre tienen el mismo valor, que corresponde al valor de la opción **ajustar a** de la ficha **Configurar impresión** del cuadro de diálogo **Configurar página** (en la ficha **diseño** , haga clic en la flecha de **Configurar página** ). 
  
Para obtener una referencia a la celda ScaleY por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ScaleY  <br/> |
   
Para obtener una referencia desde un programa a la celda ScaleY por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPrintProperties** <br/> |
|Índice de celda:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

