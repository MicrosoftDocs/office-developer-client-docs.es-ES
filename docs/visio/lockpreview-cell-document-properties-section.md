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
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822519"
---
# <a name="lockpreview-cell-document-properties-section"></a>Celda LockPreview (sección Propiedades del documento)

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
   

