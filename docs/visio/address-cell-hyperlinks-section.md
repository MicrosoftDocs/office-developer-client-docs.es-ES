---
title: Celda Address (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338552"
---
# <a name="address-cell-hyperlinks-section"></a>Celda Address (Sección de hipervínculos)

Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.
  
La dirección se puede especificar como ruta de acceso relativa en función de la ruta de acceso base definida para el documento en el cuadro **base** de hipervínculo de la ficha **Resumen** del cuadro de diálogo **propiedades** (haga clic en la pestaña **archivo** , haga clic en **información**, haga clic en * * propiedades * * y, a continuación, haga clic en **propiedades avanzadas**). Si el documento no tiene ruta de acceso base, la aplicación explorará basándose en la ruta de acceso del documento. Si éste no se ha guardado, el hipervínculo estará sin definir.
  
## <a name="remarks"></a>Comentarios

También puede establecer el valor de la celda Address en el cuadro de diálogo **Hipervínculos** (haga clic en **Hipervínculos** en la pestaña **Insertar**). 
  
Para obtener una referencia a la celda Address por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *nombre* . Dirección en la que HYPERLINK. *nombre* es el nombre de la fila de hipervínculo  <br/> |
   
Para obtener una referencia a la celda Address por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHLinkAddress** <br/> |
   

