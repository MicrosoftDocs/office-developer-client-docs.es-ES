---
title: Celda Disabled (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332581"
---
# <a name="disabled-cell-actions-section"></a>Celda Disabled (sección de acciones)

Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se deshabilita (atenúa) el nombre del comando.  <br/> |
|FALSE  <br/> |Se habilita el nombre del comando (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Disabled por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Actividades. *nombre* . DiSabled Where acciones. *nombre* es el nombre de la fila de acciones.  <br/> |
   
Para obtener una referencia desde un programa a la celda Disabled por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionDisabled** <br/> |
   

