---
title: Celda LockFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Bloquea el formato de una forma para no se pueda cambiar.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359616"
---
# <a name="lockformat-cell-protection-section"></a>Celda LockFormat (Sección de protección)

Bloquea el formato de una forma para no se pueda cambiar.
  
|**Value**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El formato no puede cambiarse.  <br/> |
| FALSE  <br/> | El formato puede cambiarse.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockFormat  <br/> |
   
Para obtener una referencia desde un programa a la celda LockFormat por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockFormat** <br/> |
   

