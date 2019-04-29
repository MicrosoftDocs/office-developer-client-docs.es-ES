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
ms.openlocfilehash: d9fe0372c44fe3b029a4d06056c8d3871c3f91e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425585"
---
# <a name="lockend-cell-protection-section"></a>Celda LockEnd (Sección Protección)

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
   

