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
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409758"
---
# <a name="lockselect-cell-protection-section"></a>Celda LockSelect (Sección de protección)

Impide que una forma pueda seleccionarse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | La forma no puede seleccionarse.  <br/> |
| FALSE  <br/> | La forma puede seleccionarse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para que LockSelect surta efecto, la casilla de verificación **Formas** debe estar activada en el cuadro de diálogo **Proteger documento**. 
  
Para obtener una referencia a la celda LockSelect por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockSelect  <br/> |
   
Para obtener una referencia desde un programa a la celda LockSelect por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockSelect** <br/> |
   

