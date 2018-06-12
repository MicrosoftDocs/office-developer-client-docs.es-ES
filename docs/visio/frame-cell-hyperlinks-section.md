---
title: Celda Frame (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm405
localization_priority: Normal
ms.assetid: f71d8737-92ef-1124-ba4a-b7e17305bd0a
description: Representa el nombre de un marco de destino cuando la aplicación se abre como documento Active en una aplicación contenedora. El valor predeterminado es una cadena vacía.
ms.openlocfilehash: b94e5efd4a3fdf53e01f7518252852214a72c766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822207"
---
# <a name="frame-cell-hyperlinks-section"></a>Celda Frame (Sección de hipervínculos)

Representa el nombre de un marco de destino cuando la aplicación se abre como documento Active en una aplicación contenedora. El valor predeterminado es una cadena vacía.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Frame por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Hipervínculo.  *nombre* . Marco where hipervínculo.  *nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia a la celda Frame por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHLinkFrame** <br/> |
   

