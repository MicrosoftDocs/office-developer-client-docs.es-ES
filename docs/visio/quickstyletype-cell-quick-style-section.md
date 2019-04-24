---
title: Celda QuickStyleType (sección estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: Determina el tipo de estilo rápido (2D, unidimensional o conector) que hereda la forma.
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282582"
---
# <a name="quickstyletype-cell-quick-style-section"></a>Celda QuickStyleType (sección estilos rápidos)

Determina el tipo de estilo rápido (2D, unidimensional o conector) que hereda la forma. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |Visio elige automáticamente  <br/> |
|1  <br/> |1-dimensional  <br/> |
|segundo  <br/> |2 dimensiones  <br/> |
|3  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **QuickStyleType** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | QuickStyleType  <br/> |
   
Para obtener una referencia desde un programa a la celda **QuickStyleType** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de celda:  <br/> |**visQuickStyleType** <br/> |
   

