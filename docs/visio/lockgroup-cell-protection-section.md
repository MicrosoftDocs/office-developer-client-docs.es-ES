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
ms.openlocfilehash: 0cb2c0653780dcb653e5903faaaa0ebf30ea9d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404312"
---
# <a name="lockgroup-cell-protection-section"></a>Celda LockGroup (sección de protección)

Bloquea un grupo de modo que no pueda desagruparse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El grupo no puede desagruparse.  <br/> |
|FALSE  <br/> |El grupo puede desagruparse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Al establecer el valor de LockGroupCell como TRUE también se evita la eliminación de las formas que son miembros del grupo.
  
Para obtener una referencia a la celda LockGroup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockGroup  <br/> |
   
Para obtener una referencia desde un programa a la celda LockGroup por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockGroup** <br/> |
   

