---
title: Celda LockBegin (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Bloquea el punto inicial (BeginX, BeginY) de una forma 1D para una ubicación específica.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359650"
---
# <a name="lockbegin-cell-protection-section"></a>Celda LockBegin (Sección de protección)

Bloquea el punto inicial (BeginX, BeginY) de una forma 1D para una ubicación específica.
  
|**Value**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El punto inicial se encuentra bloqueado.  <br/> |
| FALSE  <br/> | El punto inicial no se encuentra bloqueado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockBegin por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockBegin  <br/> |
   
Para obtener una referencia desde un programa a la celda LockBegin por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockBegin** <br/> |
   

