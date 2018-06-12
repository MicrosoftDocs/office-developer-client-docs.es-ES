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
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823534"
---
# <a name="viewmarkup-cell-document-properties-section"></a>Celda ViewMarkup (Sección de propiedades del documento)

Determina si la marca de revisión aparece en la ventana de dibujo. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |Aparece la marca de revisión en el dibujo.  <br/> |
|FALSE  <br/> |La marca de revisión no se muestra (predeterminado).  <br/> |
   
## <a name="remarks"></a>Observaciones

 Cuando está activado el seguimiento de revisiones (celda AddMarkup es TRUE), la celda ViewMarkup se establece automáticamente en TRUE y permanece así incluso después de que se ha desactivado el seguimiento de revisiones (celda AddMarkup es FALSE). El valor de la celda ViewMarkup se omite cuando la celda AddMarkup es TRUE. 
  
La celda ViewMarkup también se establece en TRUE cuando se insertan comentarios en un dibujo (con independencia de que estén o no activadas las marcas de revisión), y es necesario que sea TRUE para ver los comentarios en el dibujo.
  
Esta celda corresponde al comando **Mostrar marcas** en el grupo de **marcado** en la ficha **Revisar** . 
  
Para obtener una referencia a la celda ViewMarkup por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ViewMarkup  <br/> |
   
Para obtener una referencia a la celda ViewMarkup por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowDoc** <br/> |
|Índice de celda:  <br/> |**visDocViewMarkup** <br/> |
   

