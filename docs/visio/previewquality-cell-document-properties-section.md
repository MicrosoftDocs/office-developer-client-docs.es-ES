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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416821"
---
# <a name="previewquality-cell-document-properties-section"></a>Celda PreviewQuality (Sección de propiedades del documento)

Determina si la vista previa del dibujo tiene calidad de borrador o de detalle.
  
|**Valor**|**Calidad de la vista previa**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Borrador  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detallado  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este valor en la ficha Resumen del cuadro de diálogo Propiedades  (haga clic en el botón **Office,** haga clic en la pestaña Información, haga clic en Propiedades del documento y, a continuación, en **Propiedades avanzadas**).  
  
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
   

