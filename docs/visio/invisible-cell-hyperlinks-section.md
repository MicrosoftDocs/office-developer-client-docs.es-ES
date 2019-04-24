---
title: Celda Invisible (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Indica si un hipervínculo aparece o no en el menú contextual de una forma o página.
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348338"
---
# <a name="invisible-cell-hyperlinks-section"></a>Celda Invisible (Sección de hipervínculos)

Indica si un hipervínculo aparece o no en el menú contextual de una forma o página. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El hipervínculo no aparece como elemento de menú en el menú contextual.  <br/> |
|FALSE  <br/> |El hipervínculo sí aparece como elemento de menú en el menú contextual (predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *nombre* . Invisible donde HYPERLINK *. nombre* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
|Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visHLinkInvisible** <br/> |
   

