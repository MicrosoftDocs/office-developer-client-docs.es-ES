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
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822356"
---
# <a name="invisible-cell-hyperlinks-section"></a>Celda Invisible (sección Hipervínculos)

Indica si un hipervínculo aparece o no en el menú contextual de una forma o página. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El hipervínculo no aparece como elemento de menú en el menú contextual.  <br/> |
|FALSE  <br/> |El hipervínculo sí aparece como elemento de menú en el menú contextual (predeterminado).  <br/> |
   
## <a name="remarks"></a>Observaciones

Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *nombre* . Invisible donde hipervínculo *.name* es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
|Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visHLinkInvisible** <br/> |
   

