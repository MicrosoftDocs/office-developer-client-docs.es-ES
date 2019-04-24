---
title: Celda PreviewQuality (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356038"
---
# <a name="previewquality-cell-document-properties-section"></a>Celda PreviewQuality (Sección de propiedades del documento)

Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.
  
|**Value**|**Calidad de la vista previa**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Draft  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detallada  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor en la ficha **Resumen** del cuadro de diálogo **propiedades** (haga clic en el botón de **Office** , haga clic en la pestaña **información** , haga clic en **propiedades del documento**y, a continuación, haga clic en **propiedades avanzadas**).
  
Para obtener una referencia a la celda PreviewQuality por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PreviewQuality  <br/> |
   
Para obtener una referencia desde un programa a la celda PreviewQuality por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocPreviewQuality** <br/> |
   

