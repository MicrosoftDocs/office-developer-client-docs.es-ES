---
title: Celda QuickStyleType (sección Estilo rápido)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina el tipo de estilo rápido (2 dimensiones, 1 dimensión o conector) que hereda la forma.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410507"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Celda QuickStyleType (sección Estilo rápido)

Determina el tipo de estilo rápido (2 dimensiones, 1 dimensión o conector) que hereda la forma. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Visio elige automáticamente  <br/> |
|1  <br/> |1 dimensional  <br/> |
|2  <br/> |2 dimensiones  <br/> |
|3  <br/> |Conector  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la **celda QuickStyleType** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | QuickStyleType  <br/> |
   
Para obtener una referencia desde un programa a la **celda QuickStyleType** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de celda:  <br/> |**visQuickStyleType** <br/> |
   

