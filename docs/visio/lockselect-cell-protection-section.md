---
title: Celda LockSelect (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Impide que una forma pueda seleccionarse.
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822534"
---
# <a name="lockselect-cell-protection-section"></a>Celda LockSelect (Sección de protección)

Impide que una forma pueda seleccionarse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La forma no puede seleccionarse.  <br/> |
| FALSE  <br/> | La forma puede seleccionarse.  <br/> |
   
## <a name="remarks"></a>Comentarios

En orden para que LockSelect surta efecto, la casilla de verificación **formas** debe seleccionarse en el cuadro de diálogo **Proteger documento** . 
  
Para obtener una referencia a la celda LockSelect por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockSelect  <br/> |
   
Para obtener una referencia a la celda LockSelect por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockSelect** <br/> |
   

