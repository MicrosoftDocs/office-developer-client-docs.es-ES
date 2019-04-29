---
title: Celda Print (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Determina si las formas que pertenecen a la capa pueden imprimirse.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435218"
---
# <a name="print-cell-layers-section"></a>Celda Print (Sección de capas)

Determina si las formas que pertenecen a la capa pueden imprimirse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Los formas pueden imprimirse.  <br/> |
|FALSE  <br/> |Las formas no pueden imprimirse.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede usar la opción **Imprimir** en el cuadro de diálogo **Propiedades de las capas** para establecer este valor (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Print por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers. Print [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Print por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visDocPreviewScope** <br/> |
   

