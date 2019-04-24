---
title: Celda Description (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contiene una cadena que describe la etiqueta de acción, que aparece como información sobre herramientas cuando los usuarios sitúan el puntero sobre la etiqueta.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360237"
---
# <a name="description-cell-action-tags-section"></a>Celda Description (sección de etiquetas de acción)

Contiene una cadena que describe la etiqueta de acción, que aparece como información sobre herramientas cuando los usuarios sitúan el puntero sobre la etiqueta.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Description por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre* . Descripción donde SmartTags. *nombre* es el nombre de la fila de la etiqueta de acción.  <br/> |
   
Para obtener una referencia a la celda Description por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagDescription** <br/> |
   

