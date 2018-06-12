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
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822709"
---
# <a name="pageheight-cell-page-properties-section"></a>Celda PageHeight (Sección de propiedades de página)

Contiene el alto de la página impresa en las unidades de dibujo.
  
## <a name="remarks"></a>Observaciones

También puede establecer el alto de página en la ficha **Tamaño de página** del cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** ), o por cambiar manualmente el tamaño de la página con el mouse. 
  
Para obtener una referencia a la celda PageHeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |PageHeight  <br/> |
   
Para obtener una referencia a la celda PageHeight por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPage** <br/> |
|Índice de celda:  <br/> |**visPageHeight** <br/> |
   

