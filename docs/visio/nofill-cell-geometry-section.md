---
title: Celda NoFill (Sección de Geometría)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: Indica si un trazado puede rellenarse.
ms.openlocfilehash: 301f30b644e338ff9e597a7a7d8226b9c8a4462f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357256"
---
# <a name="nofill-cell-geometry-section"></a>Celda NoFill (Sección de Geometría)

Indica si un trazado puede rellenarse.
  
|**Value**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El trazado no se rellena aunque otros trazados de la forma estén rellenos.  <br/> |
| FALSE  <br/> | El relleno de la forma se aplica al trazado, aunque no esté cerrado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si establece la trama de relleno de una forma a cero, ninguno de sus trazados se rellena. Esta celda se utiliza para desactivar el relleno de manera selectiva para un trazado dentro de una forma.
  
Para obtener una referencia a la celda NoFill por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . NoFill donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoFill por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowComponent** <br/> |
| Índice de celda:  <br/> |**visCompNoFill** <br/> |
   

