---
title: Celda UIFormat (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Determina el formato de un campo insertado en versiones de Visio anteriores a Visio 2000.
ms.openlocfilehash: e9506404e8ccd6ae4452c10ecdcce2d4dfd7ac2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823494"
---
# <a name="uiformat-cell-text-fields-section"></a>Celda UIFormat (sección Campos de texto)

Determina el formato de un campo insertado en versiones de Visio anteriores a Visio 2000.
  
## <a name="remarks"></a>Comentarios

Esta celda no aparece en la ventana ShapeSheet. Utilice esta celda si necesita solucionar algún problema de compatibilidad con versiones anteriores, como guardar un dibujo de Visio versión 2000 en el formato de archivo de Visio versión 5.0.
  
Para obtener una referencia a la celda UIFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fields.UIFmt [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda UIFormat por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTextField** <br/> |
| Índice de fila:  <br/> |**visRowField** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visFieldUIFormat** <br/> |
   

