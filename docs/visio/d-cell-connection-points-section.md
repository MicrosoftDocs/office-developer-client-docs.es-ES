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
ms.openlocfilehash: e7bd61b8bc7a1a3b765af738681d958e2c83ba05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408176"
---
# <a name="d-cell-connection-points-section"></a>Celda D (Sección de puntos de conexión)

Celda de borrador que se puede utilizar para escribir o probar fórmulas.
  
## <a name="remarks"></a>Comentarios

Para obtener acceso a la celda D, haga clic con el botón secundario en una fila y, a continuación, haga clic **en Cambiar tipo** de fila en el menú contextual. 
  
Para obtener una referencia a la celda D por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Connections.D[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda D por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
| Índice de fila:  <br/> |**visRowConnectionPts**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visCnnctD** <br/> |
   

