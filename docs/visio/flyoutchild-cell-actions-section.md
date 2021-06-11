---
title: Celda FlyoutChild (sección Acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420867"
---
# <a name="flyoutchild-cell-actions-section"></a>Celda FlyoutChild (sección Acciones)

Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia desde otra fórmula a la celda FlyoutChild por su nombre, o desde un programa mediante la propiedad **CellsU**, use lo siguiente. 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Acciones. *nombre*  . FlyoutChildwhere Actions.  *nombre*  es el nombre de la fila Acciones  <br/> |
   
Para obtener una referencia desde un programa a la celda FlyoutChild por su índice, use la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionFlyoutChild** <br/> |
   

