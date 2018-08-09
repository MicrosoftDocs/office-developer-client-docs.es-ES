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
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822444"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>Celda LineAdjustFrom (sección Diseño de página)

Determina qué conectores dinámicos separa la aplicación si se enrutan de manera superpuesta.
  
|**Valor**|**Ajuste**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Líneas no relacionadas  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Todas las líneas  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Sin líneas  <br/> |**visPLOLineAdjustFromNone** <br/> |
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
   

