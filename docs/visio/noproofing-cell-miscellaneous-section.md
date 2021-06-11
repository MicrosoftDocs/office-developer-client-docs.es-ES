---
title: Celda NoProofing (sección Varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina si la ortografía se corrige automáticamente y si se muestran errores ortográficos para la forma seleccionada. Toma un valor booleano.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431256"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Celda NoProofing (sección Varios)

Determina si la ortografía se corrige automáticamente y si se muestran errores ortográficos para la forma seleccionada. Toma un **valor booleano.** 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La ortografía no se corrige automáticamente y los errores ortográficos no se muestran para la forma seleccionada.  <br/> |
|FALSE  <br/> |La ortografía se corrige automáticamente y los errores ortográficos se muestran para la forma seleccionada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NoProofing por su nombre desde otra fórmula o desde un programa, mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |NoProofing  <br/> |
   
Para obtener una referencia desde un programa a la celda NoProofing por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visObjNoProofing** <br/> |
   

