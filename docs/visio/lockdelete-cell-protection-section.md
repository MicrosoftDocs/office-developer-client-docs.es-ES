---
title: Celda LockDelete (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Bloquea la forma de manera que ésta no pueda ser eliminada.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423142"
---
# <a name="lockdelete-cell-protection-section"></a>Celda LockDelete (sección de protección)

Bloquea la forma de manera que ésta no pueda ser eliminada.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La forma no se puede eliminar  <br/> |
| FALSE  <br/> | La forma puede ser eliminada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockDelete por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockDelete  <br/> |
   
Para obtener una referencia desde un programa a la celda LockDelete por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockDelete** <br/> |
   

