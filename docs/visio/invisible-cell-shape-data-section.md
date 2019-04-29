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
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405320"
---
# <a name="invisible-cell-shape-data-section"></a>Celda Invisible (sección de datos de formas)

Especifica si el elemento de datos de formas es visible en la ventana **Datos de formas**. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El elemento de datos de formas no está visible.  <br/> |
| FALSE  <br/> | El elemento de datos de formas está visible.  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de esta celda corresponde a la casilla **Oculto** del cuadro de diálogo **Definir datos de formas** (haga clic con el botón secundario en la forma, seleccione **Datos** y, a continuación, haga clic en **Definir datos de formas**.
  
Para obtener una referencia a la celda Invisible por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Polyprop.  *nombre* . Invisible donde prop.  *Name* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Invisible por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionProp** <br/> |
| Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCustPropsInvis** <br/> |
   

