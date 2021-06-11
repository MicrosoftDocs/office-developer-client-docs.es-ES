---
title: Celda Type / C (Sección de puntos de conexión)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Determina el tipo de punto de conexión.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415239"
---
# <a name="type--c-cell-connection-points-section"></a>Celda Type / C (Sección de puntos de conexión)

Determina el tipo de punto de conexión.
  
|**Valor**|**Tipo**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Hacia dentro  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Exterior  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |Hacia dentro &amp; hacia fuera  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer el tipo de punto de conexión también puede elegir la herramienta **Conector**, seleccionar una forma y, a continuación, hacer clic con el botón secundario en un punto de conexión. Para ello debe ejecutar en el modo para [programadores](run-in-developer-mode-display-the-developer-tab.md). 
  
Para obtener una referencia a la celda Type / C por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Connections.Type[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Type / C por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionConnectionPts** <br/> |
|Índice de fila:  <br/> |**visRowConnectionPts**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCnnctType** (filas no extendidas) **visCnnctC** (filas extendidas)  <br/> |
   
Para obtener información sobre las filas extensibles y no extensibles, vea la fila de puntos de conexión.
  

