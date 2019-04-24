---
title: Celda QuickStyleFontColor (sección estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Determina el color de fuente de los estilos rápidos que hereda el texto de una forma del tema activo, como un entero de 0-1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282638"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>Celda QuickStyleFontColor (sección estilos rápidos)

Determina el color de fuente de los estilos rápidos que hereda el texto de una forma del tema activo, como un entero de 0-1. 
  
|||
|:-----|:-----|
|Valor  <br/> |Descripción  <br/> |
|comprendi  <br/> |El texto de la forma utiliza el color de fuente oscuro.  <br/> |
|1  <br/> |El texto de la forma usa el color de fuente claro.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **QuickStyleFontColor** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | QuickStyleFontColor  <br/> |
   
Para obtener una referencia desde un programa a la celda **QuickStyleFontColor** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
| Índice de celda:  <br/> |**visQuickStyleFontColor** <br/> |
   

