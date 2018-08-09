---
title: Celda Date (Sección de anotaciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Contiene la fecha y la hora de la última vez que se modificó el comentario.
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821935"
---
# <a name="date-cell-annotation-section"></a>Celda Date (sección Anotación)

Contiene la fecha y la hora de la última vez que se modificó el comentario. 
  
> [!NOTE]
> Esta celda se utiliza para realizar un seguimiento de los comentarios sólo cuando se abre un archivo .vsd en Microsoft Visio 2013 o al guardar un archivo .vsdx en el formato de archivo .vsd. No se usa para realizar un seguimiento de los comentarios de documentos .vsdx en Visio 2013. 
  
## <a name="remarks"></a>Comentarios

Sólo aparece la fecha en el cuadro de comentario de la interfaz de usuario.
  
Para obtener una referencia a la celda Date por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Annotation.Date [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Date por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionAnnotation** <br/> |
| Índice de fila:  <br/> |**visRowAnnotation** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visAnnotationDate** <br/> |
   

