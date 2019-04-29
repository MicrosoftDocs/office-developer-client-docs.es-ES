---
title: Celda ThemeIndex (sección Propiedades de tema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Almacena la enumeración del tema integrado de Microsoft Visio que se ha aplicado al documento como un entero. Cuando se elige un nuevo tema para el documento, la celda ThemeIndex del documento y todas las páginas y formas que contiene se actualiza con el índice del tema integrado.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411914"
---
# <a name="themeindex-cell-theme-properties-section"></a>Celda ThemeIndex (sección Propiedades de tema)

Almacena la enumeración del tema integrado de Microsoft Visio que se ha aplicado al documento como un entero. Cuando se elige un nuevo tema para el documento, la celda **ThemeIndex** del documento y todas las páginas y formas que contiene se actualiza con el índice del tema integrado. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ThemeIndex** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ThemeIndex  <br/> |
   
Para obtener una referencia desde un programa a la celda **ThemeIndex** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowThemeProperties** <br/> |
| Índice de celda:  <br/> |**visThemeIndex** <br/> |
   

