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
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338636"
---
# <a name="addmarkup-cell-document-properties-section"></a>Celda AddMarkup (Sección de propiedades del documento)

Indica si el documento se está editando con marcas de revisión.
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se está revisando el documento.  <br/> |
|FALSE  <br/> |No se está revisando el documento (opción predeterminada).  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando se establece en TRUE la celda AddMarkup, el revisor agrega las marcas y los cambios se aplican a las páginas de superposición de revisiones, no a las páginas de dibujo originales. Cuando se establece en FALSE, se desactivan las marcas y los cambios se aplican a las páginas de dibujo originales.
  
> [!NOTE]
> Puede evitar el marcado en los documentos con la función GUARD. Si la celda AddMarkup contiene la fórmula = GUARD (FALSE), el comando **seguimiento de revisiones** está deshabilitado. 
  
Esta configuración corresponde al comando **Seguimiento de revisiones** del grupo **Revisión** de la ficha **Revisar**. 
  
Para obtener una referencia a la celda AddMarkup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |AddMarkup  <br/> |
   
Para obtener una referencia a la celda AddMarkup por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowDoc** <br/> |
|Índice de celda:  <br/> |**visDocAddMarkup** <br/> |
   

