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
ms.openlocfilehash: cfd34f17eec597c306b69f76929877013b39015e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823522"
---
# <a name="verticalalign-cell-text-block-format-section"></a>Celda VerticalAlign (Sección de formato del bloque de texto)

Determina la alineación vertical del texto en el bloque de texto.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 0  <br/> | Superior  <br/> |**visVertTop** <br/> |
| 1  <br/> | En medio  <br/> |**visVertMiddle** <br/> |
| 2  <br/> | Inferior  <br/> |**visVertBottom** <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda VerticalAlign por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | VerticalAlign  <br/> |
   
Para obtener una referencia a la celda VerticalAlign por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowText** <br/> |
| Índice de celda:  <br/> |**visTxtBlkVerticalAlign** <br/> |
   

