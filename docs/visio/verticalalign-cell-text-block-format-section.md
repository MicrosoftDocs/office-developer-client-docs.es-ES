---
title: Celda VerticalAlign (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Determina la alineación vertical del texto en el bloque de texto.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425795"
---
# <a name="verticalalign-cell-text-block-format-section"></a>Celda VerticalAlign (Sección de formato del bloque de texto)

Determina la alineación vertical del texto en el bloque de texto.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Top  <br/> |**visVertTop** <br/> |
| 1  <br/> | Middle  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Hacia la parte inferior  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda VerticalAlign por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | VerticalAlign  <br/> |
   
Para obtener una referencia a la celda VerticalAlign por su índice
 desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowText** <br/> |
| Índice de celda:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

