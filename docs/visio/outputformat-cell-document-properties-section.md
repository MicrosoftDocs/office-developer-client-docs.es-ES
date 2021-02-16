---
title: Celda OutputFormat (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Determina el formato de salida de un dibujo. Las páginas de dibujo suelen tener formato para imprimirse (valor predeterminado); no obstante, el usuario puede elegir otros formatos de salida.
ms.openlocfilehash: 09fa34095772936ab1c6a3025ed1884a533f55e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413888"
---
# <a name="outputformat-cell-document-properties-section"></a>Celda OutputFormat (Sección de propiedades del documento)

Determina el formato de salida de un dibujo. Las páginas de dibujo suelen tener formato para imprimirse (valor predeterminado); no obstante, el usuario puede elegir otros formatos de salida.
  
|**Valor**|**Formato de salida**|
|:-----|:-----|
| 0  <br/> | Impresión (valor predeterminado)  <br/> |
| 1   <br/> | Presentación de diapositivas de PowerPoint  <br/> |
| 2   <br/> | Salida HTML o GIF  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda OutputFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | OutputFormat  <br/> |
   
Para obtener una referencia desde un programa a la celda OutputFormat por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocOutputFormat** <br/> |
   

