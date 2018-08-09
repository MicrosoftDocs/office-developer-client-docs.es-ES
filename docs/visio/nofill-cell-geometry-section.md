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
ms.openlocfilehash: 3f5bab76fc38b6e82aeaeee45b75bd733afdbd26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822677"
---
# <a name="nofill-cell-geometry-section"></a>Celda NoFill (sección Geometría)

Indica si un trazado puede rellenarse.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El trazado no se rellena aunque otros trazados de la forma estén rellenos.  <br/> |
| FALSE  <br/> | El relleno de la forma se aplica al trazado, aunque no esté cerrado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si establece la trama de relleno de una forma a cero, ninguno de sus trazados se rellena. Esta celda se utiliza para desactivar el relleno de manera selectiva para un trazado dentro de una forma.
  
Para obtener una referencia a la celda NoFill por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Geometría *i* . NoFill donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda NoFill por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionFirstComponent** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de fila:  <br/> |**visRowComponent** <br/> |
| Índice de celda:  <br/> |**visCompNoFill** <br/> |
   

