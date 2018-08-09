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
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822711"
---
# <a name="noshow-cell-geometry-section"></a>Celda NoShow (sección Geometría)

Indica si un trazado se muestra en la página de dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El trazo y relleno del trazado representado mediante la sección están ocultos.  <br/> |
| FALSE  <br/> | El trazo y el relleno del trazado se muestran.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NoShow por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . NoShow donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoShow por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowComponent** <br/> |
| Índice de celda:  <br/> |**visCompNoShow** <br/> |
   

