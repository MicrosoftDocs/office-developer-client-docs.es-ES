---
title: Celda NoLine (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Determina si se dibuja una línea alrededor del límite del trazado.
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357284"
---
# <a name="noline-cell-geometry-section"></a>Celda NoLine (Sección de Geometría)

Determina si se dibuja una línea alrededor del límite del trazado.
  
|**Value**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | No se dibuja una línea alrededor del límite del trazado que es el límite de una región rellena.  <br/> |
| FALSE  <br/> | Se dibuja una línea alrededor del límite de un trazado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando el color de una línea cambia a blanco, la línea sigue existiendo aunque no esté visible en un fondo blanco. Cuando se establece el valor de esta celda a TRUE, no se dibuja ninguna línea.
  
Para obtener una referencia a la celda NoLine por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . NoLine donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoLine por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowComponent** <br/> |
| Índice de celda:  <br/> |**visCompNoLine** <br/> |
   

