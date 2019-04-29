---
title: Celda EnableGrid (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Determina si la aplicación dispone las formas basándose en una cuadrícula de página, interna e invisible, cuando se configura el diseño en el cuadro de diálogo Configurar diseño. (En la ficha Diseño, en el grupo Diseño, haga clic en Redistribuir página y, a continuación, en Más opciones de diseño).
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424444"
---
# <a name="enablegrid-cell-page-layout-section"></a>Celda EnableGrid (Sección de diseño de página)

Determina si la aplicación dispone las formas basándose en una cuadrícula de página, interna e invisible, cuando se configura el diseño en el cuadro de diálogo **Configurar diseño**. (En la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).

  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Utilizar la cuadrícula de página interna.  <br/> |
|FALSE  <br/> |No utilizar la cuadrícula de página interna.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta cuadrícula de página se crea con los valores de **Espacio entre formas** y **Tamaño promedio de las formas** en el cuadro de diálogo **Espaciado del diseño y el enrutamiento**. (En la ficha **Diseño**, haga clic en la flecha de **Configurar página**, en **Diseño y enrutamiento** y, a continuación, en **Espaciado**). 
  
Si esta característica está habilitada, la aplicación alinea el punto central de cada forma colocable con el punto central de uno de los bloques de la cuadrícula de página interna. 
  
Para obtener una referencia a la celda EnableGrid por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |EnableGrid  <br/> |
   
Para obtener una referencia desde un programa a la celda EnableGrid por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOEnableGrid** <br/> |
   

