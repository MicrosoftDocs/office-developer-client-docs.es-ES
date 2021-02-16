---
title: Celda PreviewScope (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Determina si el dibujo incluye una vista previa. Si la incluye, determina si la vista previa muestra la primera página únicamente o todas las páginas del dibujo.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426509"
---
# <a name="previewscope-cell-document-properties-section"></a>Celda PreviewScope (Sección de propiedades del documento)

Determina si el dibujo incluye una vista previa. Si la incluye, determina si la vista previa muestra la primera página únicamente o todas las páginas del dibujo.
  
|**Valor**|**Ámbito de la vista previa**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Primera página  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1   <br/> | Ninguno  <br/> |**visDocPreviewScopeNone** <br/> |
| 2   <br/> | Todas las páginas  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer este  valor en la  ficha Resumen del cuadro de  diálogo Propiedades (haga clic en el botón **De Office,** haga clic en la pestaña Información, en Propiedades del documento y, a continuación, en **Propiedades avanzadas).** 
  
Para obtener una referencia a la celda PreviewScope por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PreviewScope  <br/> |
   
Para obtener una referencia desde un programa a la celda PreviewScope por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocPreviewScope** <br/> |
   

