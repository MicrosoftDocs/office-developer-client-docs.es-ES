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
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414028"
---
# <a name="lineadjustto-cell-page-layout-section"></a>Celda LineAdjustTo (Sección de diseño de página)

Determina qué conectores dinámicos se alinean uno encima de otro.
  
|**Valor**|**Cód**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Predeterminado para el estilo de enrutamiento  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1  <br/> |Líneas cercanas entre sí  <br/> |**visPLOLineAdjustToAll** <br/> |
|segundo  <br/> |Sin líneas  <br/> |**visPLOLineAdjustToNone** <br/> |
|3  <br/> |Líneas relacionadas  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineAdjustTo por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineAdjustTo  <br/> |
   
Para obtener una referencia desde un programa a la celda LineAdjustTo por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOLineAdjustTo** <br/> |
   

