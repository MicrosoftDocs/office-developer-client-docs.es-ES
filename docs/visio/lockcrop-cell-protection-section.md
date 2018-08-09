---
title: Celda LockCrop (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Bloquea un objeto desde otro programa en lugar de recortarlo con la herramienta Recortar.
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822502"
---
# <a name="lockcrop-cell-protection-section"></a>Celda LockCrop (sección Protección)

Bloquea un objeto desde otro programa en lugar de recortarlo con la herramienta **Recortar**. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La forma no se puede recortar.  <br/> |
| FALSE  <br/> | La forma se puede recortar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockCrop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockCrop  <br/> |
   
Para obtener una referencia desde un programa a la celda LockCrop por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockCrop** <br/> |
   

