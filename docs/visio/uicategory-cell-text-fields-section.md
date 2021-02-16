---
title: Celda UICategory (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Determina la categoría de un campo insertado en versiones de Visio anteriores a Visio 2000.
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434028"
---
# <a name="uicategory-cell-text-fields-section"></a>Celda UICategory (Sección de campos de texto)

Determina la categoría de un campo insertado en versiones de Visio anteriores a Visio 2000.
  
## <a name="remarks"></a>Comentarios

Esta celda no aparece en la ventana ShapeSheet. Utilice esta celda si necesita solucionar algún problema de compatibilidad con versiones anteriores, como guardar un dibujo de Visio versión 2000 en el formato de archivo de Visio versión 5.0.
  
Para obtener una referencia a la celda UICategory por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Fields.UICat[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda UICategory por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionTextField** <br/> |
| Índice de fila:  <br/> |**visRowField**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visFieldUICategory** <br/> |
   

