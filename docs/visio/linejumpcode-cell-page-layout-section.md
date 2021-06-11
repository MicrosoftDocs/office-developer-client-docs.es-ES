---
title: Celda LineJumpCode (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Determina los conectores a los que desea agregar saltos.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416254"
---
# <a name="linejumpcode-cell-page-layout-section"></a>Celda LineJumpCode (Sección de diseño de página)

Determina los conectores a los que desea agregar saltos.
  
|**Valor**|**Conectores a los que desea agregar saltos**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Ninguno  <br/> |**visPLOJumpNone** <br/> |
|1  <br/> |Líneas horizontales  <br/> |**visPLOJumpHorizontal** <br/> |
|2  <br/> |Líneas verticales  <br/> |**visPLOJumpVertical** <br/> |
|3  <br/> |Última línea enrutada  <br/> |**visPLOJumpLastRouted** <br/> |
|4   <br/> |Última línea mostrada (forma superior en *el orden z)*  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5   <br/> |Primera línea mostrada (forma en la parte inferior del *orden z)*  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineJumpCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineJumpCode  <br/> |
   
Para obtener una referencia desde un programa a la celda LineJumpCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOJumpCode** <br/> |
   

