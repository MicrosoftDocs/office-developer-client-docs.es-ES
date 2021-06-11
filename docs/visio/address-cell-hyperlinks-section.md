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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438039"
---
# <a name="address-cell-hyperlinks-section"></a>Celda Address (Sección de hipervínculos)

Especifica una dirección URL, un nombre de archivo o una ruta UNC a la que se va a saltar.
  
Puede especificar Dirección como una ruta relativa en función de la ruta de acceso base  definida para el  documento en el cuadro **base** Hipervínculo de la ficha Resumen del cuadro de diálogo Propiedades (haga clic en la pestaña Archivo, haga clic en Información **,** haga clic en ** Propiedades **y, a continuación, haga clic en **Propiedades** avanzadas ).  Si el documento no tiene ruta de acceso base, la aplicación explorará basándose en la ruta de acceso del documento. Si éste no se ha guardado, el hipervínculo estará sin definir.
  
## <a name="remarks"></a>Comentarios

También puede establecer el valor de la celda Address en el cuadro de diálogo **Hipervínculos** (haga clic en **Hipervínculos** en la pestaña **Insertar**). 
  
Para obtener una referencia a la celda Address por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *nombre*  . Dirección donde Hyperlink. *nombre*  es el nombre de la fila de hipervínculo  <br/> |
   
Para obtener una referencia a la celda Address por su nombre desde otra fórmula, o desde un programa, mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
| Índice de fila:  <br/> |**visRow1stHyperlink**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visHLinkAddress** <br/> |
   

