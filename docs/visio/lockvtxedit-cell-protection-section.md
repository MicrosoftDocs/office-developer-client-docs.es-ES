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
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822547"
---
# <a name="lockvtxedit-cell-protection-section"></a>Celda LockVtxEdit (Sección de protección)

Bloquea los vértices de una forma para que no se puedan editar.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Los vértices no se pueden editar.  <br/> |
|FALSE  <br/> |Los vértices se pueden editar.  <br/> |
   
## <a name="remarks"></a>Observaciones

Para obtener una referencia a la celda LockVtxEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockVtxEdit  <br/> |
   
Para obtener una referencia a la celda LockVtxEdit por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockVtxEdit** <br/> |
   

