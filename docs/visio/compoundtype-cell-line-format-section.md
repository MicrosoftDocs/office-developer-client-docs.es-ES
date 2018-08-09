---
title: Celda CompoundType (sección Formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Determina el tipo de la línea de una forma compuesto.
ms.openlocfilehash: 663b683030251c8b57324f1d2bdf492463c50eef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821808"
---
# <a name="compoundtype-cell-line-format-section"></a>Celda CompoundType (sección Formato de línea)

Determina el tipo de la línea de una forma compuesto. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Sencillo  <br/> |
|1  <br/> |Doble  <br/> |
|2  <br/> |Grueso fino  <br/> |
|3  <br/> |Fino grueso  <br/> |
|4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **CompoundType** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | CompoundType  <br/> |
   
Para obtener una referencia a la celda **CompoundType** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLine** <br/> |
| Índice de celda:  <br/> |**visCompoundType** <br/> |
   

