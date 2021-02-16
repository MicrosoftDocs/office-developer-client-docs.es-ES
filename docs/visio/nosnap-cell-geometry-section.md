---
title: Celda NoSnap (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Determina si otras formas se ajustan a un trazado.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408547"
---
# <a name="nosnap-cell-geometry-section"></a>Celda NoSnap (Sección de Geometría)

Determina si otras formas se ajustan a un trazado.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | No se permite que otras formas se ajusten a este trazado.  <br/> |
| FALSE  <br/> | Se permite que otras formas se ajusten a este trazado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda NoSnap por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría  *i*  . NoSnap donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoSnap por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowComponent** <br/> |
| Índice de celda:  <br/> |**visCompNoSnap** <br/> |
   

