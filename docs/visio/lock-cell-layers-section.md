---
title: Celda Lock (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.
ms.openlocfilehash: f404fe15814de802f4f6bfcebfd2558cf10cc7eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822489"
---
# <a name="lock-cell-layers-section"></a>Celda Lock (sección Capas)

Determina si las formas que pertenecen a la capa están bloqueadas de modo que no puedan seleccionarse o modificarse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Las formas están bloqueadas.  <br/> |
|FALSE  <br/> |Las formas no están bloqueadas.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede establecer este valor si selecciona **Bloquear** en el cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Lock por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Locked [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Lock por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerLock** <br/> |
   

