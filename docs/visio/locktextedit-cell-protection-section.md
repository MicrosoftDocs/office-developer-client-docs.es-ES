---
title: Celda LockTextEdit (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Bloquea el texto de una forma para que no se pueda editar.
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348317"
---
# <a name="locktextedit-cell-protection-section"></a>Celda LockTextEdit (Sección de protección)

Bloquea el texto de una forma para que no se pueda editar.
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto no se puede editar.  <br/> |
| FALSE  <br/> | El texto se puede editar.  <br/> |
   
## <a name="remarks"></a>Comentarios

No obstante, puede dar formato al texto al aplicarle un estilo mediante el cuadro de diálogo **Texto** (en la ficha **Inicio**, haga clic en la flecha de **Fuente**). 
  
Para obtener una referencia a la celda LockTextEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockTextEdit  <br/> |
   
Para obtener una referencia desde un programa a la celda LockTextEdit por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockTextEdit** <br/> |
   

