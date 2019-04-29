---
title: Celda LockVtxEdit (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Bloquea los vértices de una forma para que no se puedan editar.
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417672"
---
# <a name="lockvtxedit-cell-protection-section"></a>Celda LockVtxEdit (Sección de protección)

Bloquea los vértices de una forma para que no se puedan editar.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Los vértices no se pueden editar.  <br/> |
|FALSE  <br/> |Los vértices se pueden editar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockVtxEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockVtxEdit  <br/> |
   
Para obtener una referencia desde un programa a la celda LockVtxEdit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockVtxEdit** <br/> |
   

