---
title: Celda LockWidth (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822539"
---
# <a name="lockwidth-cell-protection-section"></a>Celda LockWidth (sección Protección)

Bloquea el ancho de la forma de manera que éste permanece inalterado al ajustar el tamaño de la forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El ancho se encuentra bloqueado.  <br/> |
| FALSE  <br/> | El ancho no se encuentra bloqueado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockWidth por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockWidth  <br/> |
   
Para obtener una referencia desde un programa a la celda LockWidth por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockWidth** <br/> |
   

