---
title: Celda Checked (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Indica si un elemento aparece activado en el menú contextual o de etiquetas de acción.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438333"
---
# <a name="checked-cell-actions-section"></a>Celda Checked (sección de acciones)

Indica si un elemento aparece activado en el menú contextual o de etiquetas de acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se muestra una marca de verificación.  <br/> |
|FALSE  <br/> |No se muestra marca de verificación (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Checked por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Actividades. *nombre* . Comprobando las acciones. *nombre* es el nombre de la fila de acciones.  <br/> |
   
Para obtener una referencia desde un programa a la celda Checked por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visActionChecked** <br/> |
   

