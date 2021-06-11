---
title: Celda TextDirection (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Determina la dirección de los caracteres de un bloque de texto.
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406230"
---
# <a name="textdirection-cell-text-block-format-section"></a>Celda TextDirection (Sección de formato del bloque de texto)

Determina la dirección de los caracteres de un bloque de texto.
  
|**Valor**|**Dirección**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Horizontal.  <br/> |**visTxtBlkLeftToRight** <br/> |
| 1  <br/> | Vertical  <br/> |**visTxtBlkTopToBottom** <br/> |
   
## <a name="remarks"></a>Comentarios

En los productos Visio versión 5.0 en japonés, el valor de esta celda se almacenaba en la celda VerticalText de la sección de varios.
  
Para obtener una referencia a la celda TextDirection por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | TextDirection  <br/> |
   
Para obtener una referencia desde un programa a la celda TextDirection por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowText** <br/> |
| Índice de celda:  <br/> |**visTxtBlkDirection** <br/> |
   

