---
title: Celda LockVariation (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina si se puede cambiar la variación de tema aplicada a la página o forma, como un valor Boolean.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427930"
---
# <a name="lockvariation-cell-protection-section"></a>Celda LockVariation (sección Protección)

Determina si se puede cambiar la variación de tema aplicada a la página o forma, como un valor Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |La variación actual aplicada a la página o forma no se puede cambiar.  <br/> |
|FALSE  <br/> |Se puede cambiar la variación de la página o la forma.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la **celda LockVariation** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockVariation  <br/> |
   
Para obtener una referencia desde un programa a la **celda LockVariation** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockVariation** <br/> |
   

