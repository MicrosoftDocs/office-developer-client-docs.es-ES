---
title: Celda LockGroup (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: Bloquea un grupo de modo que no pueda desagruparse.
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822527"
---
# <a name="lockgroup-cell-protection-section"></a>Celda LockGroup (Sección de protección)

Bloquea un grupo de modo que no pueda desagruparse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El grupo no puede desagruparse.  <br/> |
|FALSE  <br/> |El grupo puede desagruparse.  <br/> |
   
## <a name="remarks"></a>Observaciones

Al establecer el valor de LockGroupCell como TRUE también se evita la eliminación de las formas que son miembros del grupo.
  
Para obtener una referencia a la celda LockGroup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockGroup  <br/> |
   
Para obtener una referencia a la celda LockGroup por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockGroup** <br/> |
   

