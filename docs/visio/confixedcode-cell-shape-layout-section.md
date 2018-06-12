---
title: Celda ConFixedCode (Sección de diseño de la forma)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm175
localization_priority: Normal
ms.assetid: 8e7c9080-7ef1-0696-a3d2-d8f57ea5ab9b
description: Determina cuándo un conector vuelve a enrutarse.
ms.openlocfilehash: 448e721d8dd6e287c61488e28b875f76d0fa2977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821837"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Celda ConFixedCode (Sección de diseño de la forma)

Determina cuándo un conector vuelve a enrutarse.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Volver a enrutar libremente  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1  <br/> |Vuelve a enrutarse según sea necesario (nuevo enrutamiento manual)  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2  <br/> |Volver a enrutar nunca  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3  <br/> |Vuelve a enrutarse al cruzar.  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4  <br/> |Sólo para uso interno  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5  <br/> |Sólo para uso interno  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6  <br/> |Sólo para uso interno  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Notas

También puede establecer el valor de esta celda seleccionando un conector dinámico, haciendo clic en **comportamiento** en el grupo **Diseño de formas** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y, a continuación, haga clic en la ficha **conector** . 
  
Para obtener una referencia a la celda ConFixedCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ConFixedCode  <br/> |
   
Para obtener una referencia a la celda ConFixedCode por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOConFixedCode** <br/> |
   

