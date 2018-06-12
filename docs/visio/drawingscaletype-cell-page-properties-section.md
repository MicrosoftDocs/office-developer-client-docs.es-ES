---
title: Celda DrawingScaleType (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Determina la escala de dibujo seleccionada en el cuadro de diálogo Configurar página (haga clic en la flecha de Configurar página en la ficha Inicio).
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822039"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>Celda DrawingScaleType (Sección de propiedades de página)

Determina la escala de dibujo seleccionada en el cuadro de diálogo **Configurar página** (haga clic en la flecha de **Configurar página** en la ficha **Inicio** ). 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Sin escala  <br/> |**visNoScale** <br/> |
| 1  <br/> | Escala arquitectónica  <br/> |**visArchitectural** <br/> |
| 2  <br/> | Escala de obras públicas  <br/> |**visEngineering** <br/> |
| 3  <br/> | Escala personalizada  <br/> |**visScaleCustom** <br/> |
| 4  <br/> | Métrica  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | Escala de ingeniería mecánica  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda DrawingScaleType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DrawingScaleType  <br/> |
   
Para obtener una referencia a la celda DrawingScaleType por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageDrawScaleType** <br/> |
   

