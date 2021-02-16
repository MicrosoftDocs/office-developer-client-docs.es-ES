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
ms.openlocfilehash: b2b9cde309c720493f0e46962b2fe6c2e79545d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404186"
---
# <a name="confixedcode-cell-shape-layout-section"></a>Celda ConFixedCode (Sección de diseño de la forma)

Determina cuándo un conector vuelve a enrutarse.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Vuelve a enrutarse libremente.  <br/> |**visSLOConFixedRerouteFreely** <br/> |
|1   <br/> |Vuelve a enrutarse según sea necesario (nuevo enrutamiento manual).  <br/> |**visSLOConFixedRerouteAsNeeded** <br/> |
|2   <br/> |No vuelve a enrutarse nunca.  <br/> |**visSLOConFixedRerouteNever** <br/> |
|3   <br/> |Vuelve a enrutarse al cruzar.  <br/> |**visSLOConFixedRerouteOnCrossover** <br/> |
|4   <br/> |Sólo para uso interno  <br/> |**visSLOConFixedByAlgFrom** <br/> |
|5   <br/> |Sólo para uso interno  <br/> |**visSLOConFixedByAlgTo** <br/> |
|6   <br/> |Sólo para uso interno  <br/> |**visSLOConFixedByAlgFromTo** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda seleccionando un  conector dinámico, [](run-in-developer-mode-display-the-developer-tab.md) haciendo clic en Comportamiento en el grupo Diseño de formas de la ficha Programador y, a continuación, haciendo clic en la **pestaña** Conector.  
  
Para obtener una referencia a la celda ConFixedCode por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ConFixedCode  <br/> |
   
Para obtener una referencia desde un programa a la celda ConFixedCode por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowShapeLayout** <br/> |
|Índice de celda:  <br/> |**visSLOConFixedCode** <br/> |
   

