---
title: Celda LockEnd (Sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Bloquea el extremo (EndX, EndY) de una forma 1D para una ubicación específica.
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822508"
---
# <a name="lockend-cell-protection-section"></a>Celda LockEnd (sección Protección)

Bloquea el extremo (EndX, EndY) de una forma 1D para una ubicación específica.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El extremo se encuentra bloqueado.  <br/> |
| FALSE  <br/> | El extremo no se encuentra bloqueado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockEnd por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockEnd  <br/> |
   
Para obtener una referencia desde un programa a la celda LockEnd por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockEnd** <br/> |
   

