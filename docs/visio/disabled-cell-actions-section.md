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
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821976"
---
# <a name="disabled-cell-actions-section"></a>Celda Disabled (sección Acciones)

Indica si está deshabilitado un elemento de un menú contextual o de etiquetas de acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Se deshabilita (atenúa) el nombre del comando.  <br/> |
|FALSE  <br/> |Se habilita el nombre del comando (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Observaciones

Para obtener una referencia a la celda Disabled por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Acciones. *nombre* . Deshabilitado donde acciones. *nombre* es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia desde un programa a la celda Disabled por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionDisabled** <br/> |
   

