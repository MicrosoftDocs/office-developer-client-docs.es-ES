---
title: Celda Comment (Sección de anotaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Contiene el texto que aparece en un comentario.
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415533"
---
# <a name="comment-cell-annotation-section"></a>Celda Comment (sección de anotaciones)

Contiene el texto que aparece en un comentario.
  
> [!NOTE]
> Esta celda se usa para realizar el seguimiento de comentarios solo al abrir un archivo .vsd en Microsoft Visio 2013 o al guardar un archivo .vsdx en el formato de archivo .vsd. No se usa para realizar el seguimiento de comentarios en documentos .vsdx en Visio 2013. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Comment por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Annotation.Comment[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Comment por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionAnnotation** <br/> |
| Índice de fila:  <br/> |**visRowAnnotation**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visAnnotationComment** <br/> |
   

