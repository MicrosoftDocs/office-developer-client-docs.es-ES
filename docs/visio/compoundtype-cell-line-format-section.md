---
title: Celda CompoundType (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: Determina el tipo compuesto de la línea de una forma.
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407175"
---
# <a name="compoundtype-cell-line-format-section"></a>Celda CompoundType (Sección de formato de línea)

Determina el tipo compuesto de la línea de una forma. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Sencillo  <br/> |
|1   <br/> |Doble  <br/> |
|2   <br/> |Grueso fino  <br/> |
|3   <br/> |Grosor fino  <br/> |
|4   <br/> |Triple  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **CompoundType** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell,** o desde un programa mediante la propiedad **CellsU,** utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | CompoundType  <br/> |
   
Para obtener una referencia desde un programa a **la celda CompoundType** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLine** <br/> |
| Índice de celda:  <br/> |**visCompoundType** <br/> |
   

