---
title: Celda LockFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Bloquea el formato de una forma para no se pueda cambiar.
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822507"
---
# <a name="lockformat-cell-protection-section"></a>Celda LockFormat (Sección de protección)

Bloquea el formato de una forma para no se pueda cambiar.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El formato no puede cambiarse.  <br/> |
| FALSE  <br/> | El formato puede cambiarse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockFormat  <br/> |
   
Para obtener una referencia a la celda LockFormat por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockFormat** <br/> |
   

