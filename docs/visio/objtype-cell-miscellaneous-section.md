---
title: Celda ObjType (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Determina si los objetos son colocables o enrutables en diagramas cuando se disponen las formas con el comando Configurar diseño.
ms.openlocfilehash: 7a607fdb53ad569e84976b6f9911fbd89f7f2628
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361015"
---
# <a name="objtype-cell-miscellaneous-section"></a>Celda ObjType (Sección de varios)

Determina si los objetos son colocables o enrutables en diagramas cuando se disponen las formas con el comando **Configurar diseño**. 
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Éste es el valor predeterminado. La aplicación decide según el contexto del dibujo.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |La forma es colocable.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |La forma es enrutable. Debe ser una forma unidimensional (1D).  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |La forma no es colocable ni enrutable.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |El grupo contiene formas colocables o enrutables.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Comentarios

De manera predeterminada, la celda ObjType se establece a No Formula para una forma. Esto equivale a 0, que significa que la aplicación determina si la forma puede ser colocable según su contexto. Por ejemplo, si dibuja un rectángulo simple, el valor de su celda ObjType es 0. Si, a continuación, usa la herramienta **Conector** para conectar el rectángulo a otra forma, Visio restablece el valor de la celda ObjType del rectángulo a 1 (colocable). 
  
El valor de la celda ObjType puede ser una combinación de valores. Sin embargo, si el bit no colocable&amp;está establecido (H4), tiene prioridad sobre otros valores excepto el valor de grupo&amp;(H8).
  
Para obtener una referencia a la celda ObjType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ObjType  <br/> |
   
Para obtener una referencia desde un programa a la celda ObjType por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visLOFlags** <br/> |
   

