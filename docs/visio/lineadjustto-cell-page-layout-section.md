---
title: Celda LineAdjustTo (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Determina qué conectores dinámicos se alinean uno encima de otro.
ms.openlocfilehash: 13540f9dc5e6e6861d3f3679bcf49204d553397a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822455"
---
# <a name="lineadjustto-cell-page-layout-section"></a>Celda LineAdjustTo (Sección de diseño de página)

Determina qué conectores dinámicos se alinean uno encima de otro.
  
|**Valor**|**Ajuste**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Predeterminado para el estilo de enrutamiento  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Líneas cercanas entre sí  <br/> |**visPLOLineAdjustToAll** <br/> |
|2  <br/> |Sin líneas  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Líneas relacionadas  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Notas

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** en el cuadro de diálogo **Configurar página** (en la ficha **Diseño** , haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineAdjustTo por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineAdjustTo  <br/> |
   
Para obtener una referencia a la celda LineAdjustTo por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOLineAdjustTo** <br/> |
   

