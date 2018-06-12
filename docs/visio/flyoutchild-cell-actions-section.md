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
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822161"
---
# <a name="flyoutchild-cell-actions-section"></a>Celda FlyoutChild (sección Acciones)

Determina si la fila es un menú emergente secundario de la última fila por encima de ella que no es un elemento secundario emergente. 
  
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda FlyoutChild por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , use lo siguiente. 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Acciones. *nombre* . Acciones de FlyoutChildwhere.  *nombre* es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia a la celda FlyoutChild por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionFlyoutChild** <br/> |
   

