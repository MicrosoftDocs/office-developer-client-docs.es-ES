---
title: Celda CompoundType (sección formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Determina el tipo compuesto de la línea de una forma.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359376"
---
# <a name="compoundtype-cell-line-format-section"></a>Celda CompoundType (sección formato de línea)

Determina el tipo compuesto de la línea de una forma. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |Sencillo  <br/> |
|1  <br/> |Doble  <br/> |
|segundo  <br/> |Gruesa fina  <br/> |
|3  <br/> |Gruesa fina  <br/> |
|4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **CompoundType** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | CompoundType  <br/> |
   
Para obtener una referencia desde un programa a la celda **CompoundType** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLine** <br/> |
| Índice de celda:  <br/> |**visCompoundType** <br/> |
   

