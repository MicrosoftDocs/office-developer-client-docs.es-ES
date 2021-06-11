---
title: Celda X (Sección de anotación)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: La coordenada x del marcador de comentario en coordenadas de página.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434483"
---
# <a name="x-cell-annotation-section"></a>Celda X (Sección de anotación)

La coordenada  *x*  del marcador de comentario en coordenadas de página. 
  
> [!NOTE]
> Esta celda se usa para realizar el seguimiento de comentarios solo al abrir un archivo .vsd en Microsoft Visio 2013 o al guardar un archivo .vsdx en el formato de archivo .vsd. No se usa para realizar el seguimiento de comentarios en documentos .vsdx en Visio 2013. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda X por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Annotation.X[  *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda X por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionAnnotation** <br/> |
| Índice de fila:  <br/> |**visRowAnnotation**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visAnnotationX** <br/> |
   

