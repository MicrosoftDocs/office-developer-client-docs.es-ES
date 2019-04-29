---
title: Celda Comment (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
localization_priority: Normal
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: Contiene el texto de comentario en formato de cadena para una forma.
ms.openlocfilehash: e6f21875928bce31dc2004d88f2d281e31265d65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419068"
---
# <a name="comment-cell-miscellaneous-section"></a>Celda Comment (Sección de varios)

Contiene el texto de comentario en formato de cadena para una forma.
  
## <a name="remarks"></a>Comentarios

También puede insertar un comentario haciendo clic en **Nuevo comentario** en la ficha **Revisar**. 
  
Para obtener una referencia a la celda Comment por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Comentario  <br/> |
   
Para obtener una referencia desde un programa a la celda Comment por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowMisc** <br/> |
|Índice de celda:  <br/> |**visComment** <br/> |
   

