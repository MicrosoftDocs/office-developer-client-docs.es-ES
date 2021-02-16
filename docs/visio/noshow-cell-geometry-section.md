---
title: Celda NoShow (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indica si un trazado se muestra en la página de dibujo.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410353"
---
# <a name="noshow-cell-geometry-section"></a>Celda NoShow (Sección de Geometría)

Indica si un trazado se muestra en la página de dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El trazo y relleno del trazado representado mediante la sección están ocultos.  <br/> |
| FALSE  <br/> | El trazo y el relleno del trazado se muestran.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NoShow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría  *i*  . NoShow donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoShow por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowComponent** <br/> |
| Índice de celda:  <br/> |**visCompNoShow** <br/> |
   

