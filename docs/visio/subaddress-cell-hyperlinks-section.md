---
title: Celda SubAddress (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Especifica una ubicación del documento de destino con la que se establece el vínculo.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349325"
---
# <a name="subaddress-cell-hyperlinks-section"></a>Celda SubAddress (Sección de hipervínculos)

Especifica una ubicación del documento de destino con la que se establece el vínculo.
  
## <a name="remarks"></a>Comentarios

Por ejemplo, si la celda address es "Drawing1. vsdx", la celda subAddress puede especificar un nombre de página como "Page-3". Si la celda address es el archivo de Microsoft Excel "Samples. xlsx", el valor de esta celda puede ser una hoja de cálculo o un rango de una hoja de cálculo, como "funciones de hoja de cálculo" o "Hoja1! A1: D10 ". Si la celda address es "https://www.microsoft.com/office/", el valor de esta celda puede ser un anclaje con nombre dentro del documento, como "soluciones".
  
También puede establecer el valor de esta celda en el cuadro de diálogo ** Hipervínculos** (en el grupo **Vínculos** en la ficha **Insertar**, haga clic en **Hipervínculo**).
  
Para obtener una referencia a la celda SubAddress por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Hipervínculo.  *nombre* . Subdirección donde HYPERLINK *. nombre* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un **** programa a la celda SubAddress por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHLinkSubAddress** <br/> |
   

