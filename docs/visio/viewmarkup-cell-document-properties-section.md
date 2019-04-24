---
title: Celda ViewMarkup (Sección de propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Determina si la marca de revisión aparece en la ventana de dibujo.
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355828"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Celda ViewMarkup (Sección de propiedades del documento)

Determina si la marca de revisión aparece en la ventana de dibujo. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Aparece la marca de revisión en el dibujo.  <br/> |
|FALSE  <br/> |La marca de revisión no se muestra (predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

 Cuando se activa el seguimiento de revisiones (la celda AddMarkup es TRUE), la celda ViewMarkup se establece automáticamente en TRUE y sigue siendo TRUE incluso después de que se haya desactivado el seguimiento de revisiones (la celda AddMarkup es FALSE). Se omite el valor de la celda ViewMarkup cuando el valor de AddMarkup es TRUE. 
  
La celda ViewMarkup también se establece en TRUE cuando se insertan comentarios en un dibujo (con independencia de que estén o no activadas las marcas de revisión), y es necesario que sea TRUE para ver los comentarios en el dibujo.
  
Esta celda corresponde al comando **Mostrar marcas** en el grupo **Revisión** de la ficha **Revisar**. 
  
Para obtener una referencia a la celda ViewMarkup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ViewMarkup  <br/> |
   
Para obtener una referencia desde un programa a la celda ViewMarkup por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowDoc** <br/> |
|Índice de celda:  <br/> |**visDocViewMarkup** <br/> |
   

