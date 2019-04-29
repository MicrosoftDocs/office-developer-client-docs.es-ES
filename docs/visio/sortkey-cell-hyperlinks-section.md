---
title: Celda SortKey (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Un número que determina el orden de los hipervínculos que aparecen en un menú contextual.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406384"
---
# <a name="sortkey-cell-hyperlinks-section"></a>Celda SortKey (Sección de hipervínculos)

Un número que determina el orden de los hipervínculos que aparecen en un menú contextual.
  
## <a name="remarks"></a>Comentarios

Los hipervínculos aparecen en un menú contextual ordenadas de menor a mayor, con los números más bajos en la parte superior del menú. Si dos filas de hipervínculos tienen el mismo valor para la celda SortKey, el orden queda determinado por el orden físico de la fila. El valor predeterminado es 0 (cero). 
  
Para obtener una referencia a la celda SortKey por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *nombre* . SortKey donde HYPERLINK *. nombre* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda SortKey por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
|Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visHLinkSortKey** <br/> |
   

