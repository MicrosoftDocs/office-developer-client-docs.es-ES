---
title: Celda LockAspect (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Bloquea la relación de aspecto de la forma de manera que solo se puede ajustar el tamaño de manera proporcional; no se puede ajustar el tamaño en una única dimensión.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359643"
---
# <a name="lockaspect-cell-protection-section"></a>Celda LockAspect (Sección de protección)

Bloquea la relación de aspecto de la forma de manera que solo se puede ajustar el tamaño de manera proporcional; no se puede ajustar el tamaño en una única dimensión.
  
|**Value**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La relación de aspecto se encuentra bloqueada.  <br/> |
| FALSE  <br/> | La relación de aspecto no se encuentra bloqueada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockAspect por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**,utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockAspect  <br/> |
   
Para obtener una referencia desde un programa a la celda LockAspect por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockAspect** <br/> |
   

