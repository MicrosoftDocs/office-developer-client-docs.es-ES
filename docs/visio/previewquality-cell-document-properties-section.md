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
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822838"
---
# <a name="previewquality-cell-document-properties-section"></a>Celda PreviewQuality (Sección de propiedades del documento)

Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.
  
|**Valor**|**Calidad de la vista previa**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Borrador  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detallada  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Notas

También puede establecer este valor en la ficha **Resumen** en el cuadro de diálogo **Propiedades** (haga clic en el botón de **Office** , haga clic en la ficha **información** , haga clic en **Propiedades del documento**y, a continuación, haga clic en **Propiedades avanzadas**).
  
Para obtener una referencia a la celda PreviewQuality por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PreviewQuality  <br/> |
   
Para obtener una referencia a la celda PreviewQuality por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocPreviewQuality** <br/> |
   

