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
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822059"
---
# <a name="enablegrid-cell-page-layout-section"></a>Celda EnableGrid (sección Diseño de página)

Determina si la aplicación dispone las formas basándose en una cuadrícula de página, interna e invisible, cuando se configura el diseño en el cuadro de diálogo **Configurar diseño**. (En la ficha **Diseño**, en el grupo **Diseño**, haga clic en **Redistribuir página** y, a continuación, en **Más opciones de diseño**).

  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Utilizar la cuadrícula de página interna.  <br/> |
|FALSE  <br/> |No utilizar la cuadrícula de página interna.  <br/> |
   
## <a name="remarks"></a>Observaciones

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
   

