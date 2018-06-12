---
title: Celda LockVariation (sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina si se puede cambiar la variación de tema aplicada a la forma o página, como un valor Boolean.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822549"
---
# <a name="lockvariation-cell-protection-section"></a>Celda LockVariation (sección de protección)

Determina si se puede cambiar la variación de tema aplicada a la forma o página, como un valor Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |No se puede cambiar la variante actual aplicada a la forma o página.  <br/> |
|FALSE  <br/> |La variación de la página o la forma se puede cambiar.  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda **LockVariation** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockVariation  <br/> |
   
Para obtener una referencia a la celda **LockVariation** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockVariation** <br/> |
   

