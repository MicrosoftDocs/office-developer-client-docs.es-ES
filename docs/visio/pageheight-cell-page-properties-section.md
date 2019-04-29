---
title: Celda PageHeight (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Contiene el alto de la página impresa en las unidades de dibujo.
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427083"
---
# <a name="pageheight-cell-page-properties-section"></a>Celda PageHeight (sección de propiedades de página)

Contiene el alto de la página impresa en las unidades de dibujo.
  
## <a name="remarks"></a>Comentarios

También puede establecer el alto de la página en la ficha **Tamaño de página** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**) o manualmente cambiando el tamaño de la página con el mouse. 
  
Para obtener una referencia a la celda PageHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PageHeight  <br/> |
   
Para obtener una referencia desde un programa a la celda PageHeight por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPage** <br/> |
|Índice de celda:  <br/> |**visPageHeight** <br/> |
   

