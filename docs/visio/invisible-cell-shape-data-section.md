---
title: Celda Invisible (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Especifica si el elemento de datos de formas es visible en la ventana Datos de formas.
ms.openlocfilehash: 2cd3fcad5db7b1752c55055354f1ec842bff4899
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822346"
---
# <a name="invisible-cell-shape-data-section"></a>Celda Invisible (sección Datos de forma)

Especifica si el elemento de datos de formas es visible en la ventana **Datos de formas**. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El elemento de datos de formas no está visible.  <br/> |
| FALSE  <br/> | El elemento de datos de formas está visible.  <br/> |
   
## <a name="remarks"></a>Observaciones

El valor de esta celda corresponde a la casilla **Oculto** del cuadro de diálogo **Definir datos de formas** (haga clic con el botón secundario en la forma, seleccione **Datos** y, a continuación, haga clic en **Definir datos de formas**.
  
Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | De propiedades.  *nombre* . Where invisible de propiedades.  *nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsInvis** <br/> |
   

