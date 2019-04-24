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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359293"
---
# <a name="outputformat-cell-document-properties-section"></a>Celda OutputFormat (Sección de propiedades del documento)

Determina el formato de salida de un dibujo. Las páginas de dibujo suelen tener formato para imprimirse (valor predeterminado); no obstante, el usuario puede elegir otros formatos de salida.
  
|**Value**|**Formato de salida**|
|:-----|:-----|
| comprendi  <br/> | Impresión (valor predeterminado)  <br/> |
| 1  <br/> | Presentación de diapositivas de PowerPoint  <br/> |
| segundo  <br/> | Salida HTML o GIF  <br/> |
   
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
   

