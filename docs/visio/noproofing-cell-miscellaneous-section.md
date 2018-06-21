---
title: Celda NoProofing (sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina si se ha corregido automáticamente ortografía y si se muestran los errores de ortografía para la forma seleccionada. Toma un valor booleano.
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/21/2018
ms.locfileid: "19822678"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Celda NoProofing (sección de varios)

Determina si se ha corregido automáticamente ortografía y si se muestran los errores de ortografía para la forma seleccionada. Toma un valor **booleano** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Ortografía no se corrige automáticamente y no se muestran errores de ortografía para la forma seleccionada.  <br/> |
|FALSE  <br/> |Ortografía se corrige automáticamente y se muestran los errores de ortografía para la forma seleccionada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NoProofing por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |NoProofing  <br/> |
   
Para obtener una referencia a la celda NoProofing por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visObjNoProofing** <br/> |
   

