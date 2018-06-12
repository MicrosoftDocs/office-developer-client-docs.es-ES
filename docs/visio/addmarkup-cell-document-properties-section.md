---
title: Celda AddMarkup (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Indica si el documento se está editando con marcas de revisión.
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821530"
---
# <a name="addmarkup-cell-document-properties-section"></a>Celda AddMarkup (Sección de propiedades del documento)

Indica si el documento se está editando con marcas de revisión.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se está revisando el documento.  <br/> |
|FALSE  <br/> |No se está revisando el documento (opción predeterminada).  <br/> |
   
## <a name="remarks"></a>Observaciones

Cuando se establece la celda AddMarkup es true, el revisor agrega las marcas y los cambios se aplican a páginas de revisión superpuestas, no a las páginas de dibujo originales. Cuando la celda AddMarkup es FALSE, el seguimiento de revisiones está desactivado y los cambios se aplican a las páginas de dibujo originales.
  
> [!NOTE]
> Puede evitar marcado en los documentos mediante la función GUARD. Si la celda AddMarkup contiene la fórmula = GUARD (false), el comando **Seguimiento de revisiones** está deshabilitado. 
  
Esta configuración corresponde a la opción de comando **Seguimiento de revisiones** en el grupo de **marcado** en la ficha **Revisar** . 
  
Para obtener una referencia a la celda AddMarkup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |AddMarkup  <br/> |
   
Para obtener una referencia a la celda AddMarkup por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowDoc** <br/> |
|Índice de celda:  <br/> |**visDocAddMarkup** <br/> |
   

