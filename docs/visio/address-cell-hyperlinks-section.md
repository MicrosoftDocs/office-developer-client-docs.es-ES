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
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821534"
---
# <a name="address-cell-hyperlinks-section"></a>Celda Address (sección Hipervínculos)

Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.
  
Puede especificar la dirección como una ruta de acceso relativa basada en la ruta de acceso base definida para el documento en el cuadro **base de hipervínculo** en la ficha **Resumen** del cuadro de diálogo **Propiedades** (haga clic en la pestaña **archivo** , haga clic en **información**, haga clic en ** Propiedades ** y, a continuación, haga clic en **Propiedades avanzadas**). Si el documento no tiene ninguna ruta de acceso base, la aplicación se desplaza en función de la ruta de acceso del documento. Si no se ha guardado el documento, el hipervínculo no está definido.
  
## <a name="remarks"></a>Comentarios

También puede establecer el valor de la celda Address en el cuadro de diálogo **Hipervínculos** (haga clic en **Hipervínculos** en la pestaña **Insertar**). 
  
Para obtener una referencia a la celda Address por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *nombre* . Direcciones where hipervínculo. *nombre* es el nombre de la fila de hipervínculo  <br/> |
   
Para obtener una referencia a la celda Address por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHLinkAddress** <br/> |
   

