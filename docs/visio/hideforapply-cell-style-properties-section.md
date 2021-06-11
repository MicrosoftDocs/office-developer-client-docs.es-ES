---
title: Celda HideForApply (Sección de propiedades de estilo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Determina dónde se muestra un estilo en la interfaz Visio usuario de Microsoft.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423247"
---
# <a name="hideforapply-cell-style-properties-section"></a>Celda HideForApply (Sección de propiedades de estilo)

Determina dónde se muestra un estilo en la interfaz Visio usuario de Microsoft.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Muestra el estilo solo en **Explorador de dibujos**.  <br/> |
| FALSE  <br/> | Muestra el estilo en **Explorador de dibujos**.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si basa un estilo nuevo en un estilo oculto, el nuevo estilo no heredará dicho atributo.
  
Para obtener una referencia a la celda HideForApply por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | HideForApply  <br/> |
   
Para obtener una referencia desde un programa a la celda HideForApply por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowStyle** <br/> |
| Índice de celda:  <br/> |**visStyleHidden** <br/> |
   

