---
title: Celda LineAdjustFrom (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Determina qué conectores dinámicos separa la aplicación si se enrutan de manera superpuesta.
ms.openlocfilehash: 3eb9f5513ee3ce2f5dce96cb47c356bca29a289c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359328"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>Celda LineAdjustFrom (Sección de diseño de página)

Determina qué conectores dinámicos separa la aplicación si se enrutan de manera superpuesta.
  
|**Value**|**Cód**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Líneas no relacionadas  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Todas las líneas  <br/> |**visPLOLineAdjustFromAll** <br/> |
|segundo  <br/> |Sin líneas  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Predeterminado para el estilo de enrutamiento  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda en la ficha **Diseño y enrutamiento** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página** y, a continuación, haga clic en **Diseño y enrutamiento**).
  
Para obtener una referencia a la celda LineAdjustFrom por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LineAdjustFrom  <br/> |
   
Para obtener una referencia desde un programa a la celda LineAdjustFrom por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowPageLayout** <br/> |
|Índice de celda:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

