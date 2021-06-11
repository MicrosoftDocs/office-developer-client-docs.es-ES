---
title: Celda TxtLocPinX (Sección de transformación de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Determina la coordenada x del centro de rotación del bloque de texto en relación con el origen del bloque de texto. La fórmula predeterminada es:'
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425858"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>Celda TxtLocPinX (Sección de transformación de texto)

Determina la coordenada  *x*  del centro de rotación del bloque de texto en relación con el origen del bloque de texto. La fórmula predeterminada es: 
  
= TxtWidth \* 0.5
  
Esta fórmula da como resultado el centro horizontal del bloque de texto.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda TxtLocPinX por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TxtLocPinX  <br/> |
   
Para obtener una referencia desde un programa a la celda TxtLocPinX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowTextXForm** <br/> |
| Índice de celda:  <br/> |**visXFormLocPinX** <br/> |
   

