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
ms.openlocfilehash: 8f41e5bf854e31e1f17eabb2aecbded55175ebaf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432859"
---
# <a name="frame-cell-hyperlinks-section"></a>Celda Frame (Sección de hipervínculos)

Representa el nombre de un marco de destino cuando la aplicación se abre como documento Active en una aplicación contenedora. El valor predeterminado es una cadena vacía.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Frame por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Hipervínculo.  *nombre* . Marco en el que HYPERLINK.  *Name* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Frame por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHLinkFrame** <br/> |
   

