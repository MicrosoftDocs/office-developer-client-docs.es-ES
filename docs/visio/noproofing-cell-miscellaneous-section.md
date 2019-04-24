---
title: Celda noProofing (sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: Determina si la ortografía se corrige automáticamente y si se muestran errores de ortografía para la forma seleccionada. Toma un valor Boolean.
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357228"
---
# <a name="noproofing-cell-miscellaneous-section"></a>Celda noProofing (sección de varios)

Determina si la ortografía se corrige automáticamente y si se muestran errores de ortografía para la forma seleccionada. Toma un valor **Boolean** . 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La ortografía no se corrige automáticamente y no se muestran los errores de ortografía de la forma seleccionada.  <br/> |
|FALSE  <br/> |La ortografía se corrige automáticamente y se muestran los errores de ortografía de la forma seleccionada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda noProofing por su nombre desde otra fórmula, o desde un programa, mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |NoProofing  <br/> |
   
Para obtener una referencia desde un programa a la celda noProofing por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visObjNoProofing** <br/> |
   

