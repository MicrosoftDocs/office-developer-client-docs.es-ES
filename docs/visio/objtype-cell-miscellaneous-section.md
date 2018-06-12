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
description: Determina si los objetos son colocables o enrutables en diagramas cuando se usa el cuadro de diálogo Configurar diseño para diseñar las formas.
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822703"
---
# <a name="objtype-cell-miscellaneous-section"></a>Celda ObjType (Sección de varios)

Determina si los objetos son colocables o enrutables en diagramas cuando se usa el cuadro de diálogo **Configurar diseño** para diseñar las formas. 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Valor predeterminado. La aplicación decide según el contexto del dibujo.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |La forma es colocable.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |La forma es enrutable. Debe ser una forma unidimensional (1D).  <br/> |**Crea** <br/> |
|&amp;H4  <br/> |La forma no es colocable ni enrutable.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |El grupo contiene formas colocables o enrutables.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Notas

De forma predeterminada, la celda ObjType se establece a No Formula para una forma, que se evalúa como 0, lo que significa que la aplicación determina si la forma puede ser colocable según su contexto. Por ejemplo, si dibuja un rectángulo simple, el valor de su celda ObjType es 0. Si, a continuación, use la herramienta **conector** para conectar el rectángulo a otra forma, Visio restablece el valor de su celda ObjType del rectángulo en 1 (que puede colocarse). 
  
El valor de la celda ObjType puede ser una combinación de valores. Si está establecido el bit no colocable (&amp;H4), sin embargo, tiene prioridad sobre otros valores excepto el valor de grupo (&amp;H8).
  
Para obtener una referencia a la celda ObjType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ObjType  <br/> |
   
Para obtener una referencia a la celda ObjType por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visLOFlags** <br/> |
   

