---
title: Celda LockPreview (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Determina si una vista previa se guarda automáticamente al guardar un dibujo.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418865"
---
# <a name="lockpreview-cell-document-properties-section"></a>Celda LockPreview (sección de propiedades del documento)

Determina si una vista previa se guarda automáticamente al guardar un dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | No guardar una vista previa cada vez que se guarde un dibujo.  <br/> |
| FALSE  <br/> | Guardar una vista previa cada vez que se guarde un dibujo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LockPreview por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockPreview  <br/> |
   
Para obtener una referencia desde un programa a la celda LockPreview por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocLockPreview** <br/> |
   

