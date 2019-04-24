---
title: Celda DefaultTabstop (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Determina el intervalo de las tabulaciones predeterminadas de un bloque de texto.
ms.openlocfilehash: 1ae923f6373b9cee76238b1fb27ec5eb3acb43ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360273"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>Celda DefaultTabstop (Sección de formato del bloque de texto)

Determina el intervalo de las tabulaciones predeterminadas de un bloque de texto. 
  
## <a name="remarks"></a>Comentarios

El valor predeterminado es de 0,5 pulgadas para los documentos creados con unidades de medida anglosajonas y de 1,5 centímetros para los documentos creados con unidades métricas.
  
Para obtener una referencia a la celda DefaultTabstop por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |DefaultTabstop  <br/> |
   
Para obtener una referencia desde un programa a la celda DefaultTabstop por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowText** <br/> |
|Índice de celda:  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

