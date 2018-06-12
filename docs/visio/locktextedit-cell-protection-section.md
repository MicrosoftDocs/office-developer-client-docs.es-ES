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
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822530"
---
# <a name="locktextedit-cell-protection-section"></a>Celda LockTextEdit (Sección de protección)

Bloquea el texto de una forma para que no se pueda editar.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto no se puede editar.  <br/> |
| FALSE  <br/> | El texto se puede editar.  <br/> |
   
## <a name="remarks"></a>Observaciones

Todavía se puede formatear texto, aplicando un estilo en el cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ). 
  
Para obtener una referencia a la celda LockTextEdit por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockTextEdit  <br/> |
   
Para obtener una referencia a la celda LockTextEdit por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockTextEdit** <br/> |
   

