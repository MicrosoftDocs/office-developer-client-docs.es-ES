---
title: Celda Active (Sección de capas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Especifica si la capa está activa. Las formas sin capas preasignadas se asignan a las capas activas cuando se colocan en la página de dibujo.
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417437"
---
# <a name="active-cell-layers-section"></a>Celda Active (Sección de capas)

Especifica si la capa está activa. Las formas sin capas preasignadas se asignan a las capas activas cuando se colocan en la página de dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La capa está activa.  <br/> |
|FALSE  <br/> |La capa no está activa.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta celda corresponde a la opción **Activar** del cuadro de diálogo **Propiedades de las capas** (en el grupo **Edición**, en la ficha **Inicio**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Active por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Layers.Active[ *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Active por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionLayer** <br/> |
|Índice de fila:  <br/> |**visRowLayer**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visLayerActive** <br/> |
   

