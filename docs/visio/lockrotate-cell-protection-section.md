---
title: Celda LockRotate (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: Bloquea las formas bidimensionales para que no se puedan girar con los controladores de rotación ni con los comandos Girar 90 a la izquierda o Girar 90 a la derecha.
ms.openlocfilehash: 36da1868e4f974bd19d00e86e31bea96eb8ad5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404676"
---
# <a name="lockrotate-cell-protection-section"></a>Celda LockRotate (Sección de protección)

Bloquea las formas bidimensionales para que no se puedan girar con los controladores de rotación ni con los comandos **Girar 90 a la izquierda** o **Girar 90 a la derecha**. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La forma no se puede girar.  <br/> |
| FALSE  <br/> | La forma se puede girar (opción predeterminada).  <br/> |
   
## <a name="remarks"></a>Comentarios

La celda LockRotate no impide que las formas unidimensionales se puedan girar al arrastrar un extremo. Para bloquear la rotación de las formas unidimensionales, establezca la celda LockWidth en un valor distinto de cero (TRUE).
  
Para obtener una referencia a la celda LockRotate por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockRotate  <br/> |
   
Para obtener una referencia desde un programa a la celda LockRotate por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockRotate** <br/> |
   

