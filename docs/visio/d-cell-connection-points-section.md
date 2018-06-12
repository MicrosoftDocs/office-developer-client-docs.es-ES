---
title: Celda D (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: Celda de borrador que se puede utilizar para escribir o probar fórmulas.
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821904"
---
# <a name="d-cell-connection-points-section"></a>Celda D (Sección de puntos de conexión)

Celda de borrador que se puede utilizar para escribir o probar fórmulas.
  
## <a name="remarks"></a>Comentarios

Para obtener acceso a la celda D, haga clic en una fila y, a continuación, haga clic en **Cambiar tipo de fila** en el menú contextual. 
  
Para obtener una referencia a la celda D por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Connections.D [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda D por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
| Índice de fila:  <br/> |**visRowConnectionPts** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCnnctD** <br/> |
   

