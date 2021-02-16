---
title: Celda ResizePage (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Determina si se debe agrandar la página para acomodar el dibujo después de diseñar las formas mediante el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438095"
---
# <a name="resizepage-cell-page-layout-section"></a>Celda ResizePage (Sección de diseño de página)

Determina si se va a ampliar la página para incluir  el dibujo después de  diseñar las formas mediante  el cuadro de diálogo Configurar diseño (en la ficha Diseño, en el grupo Diseño, haga clic en Volver a diseñar página y, a continuación, haga clic en Más opciones de diseño **).** 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Se agranda la página.  <br/> |
| FALSE  <br/> | No se agranda la página.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda ResizePage por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ResizePage  <br/> |
   
Para obtener una referencia desde un programa a la celda ResizePage por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOResizePage** <br/> |
   

