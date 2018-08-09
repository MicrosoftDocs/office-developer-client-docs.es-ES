---
title: Celda ThemeIndex (sección Propiedades de tema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Almacena la enumeración del tema de Microsoft Visio integrada aplicado al documento, como un número entero. Cuando se elige un nuevo tema para el documento, la celda ThemeIndex para el documento y todas las páginas y las formas que contiene se actualiza con el índice del tema integrado.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823390"
---
# <a name="themeindex-cell-theme-properties-section"></a>Celda ThemeIndex (sección Propiedades de tema)

Almacena la enumeración del tema de Microsoft Visio integrada aplicado al documento, como un número entero. Cuando se elige un nuevo tema para el documento, la celda **ThemeIndex** para el documento y todas las páginas y las formas que contiene se actualiza con el índice del tema integrado. 
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **ThemeIndex** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ThemeIndex  <br/> |
   
Para obtener una referencia a la celda **ThemeIndex** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowThemeProperties** <br/> |
| Índice de celda:  <br/> |**visThemeIndex** <br/> |
   

