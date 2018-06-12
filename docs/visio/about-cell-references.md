---
title: Referencias a celdas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251827
localization_priority: Normal
ms.assetid: e6a9aceb-90d7-fb53-eaf4-416a1ae2a98b
description: Puede crear dependencias entre fórmulas por medio de las referencias a celdas de ShapeSheet. Las referencias a celdas le dan la posibilidad de calcular el valor de una celda basándose en el valor de otra. Por ejemplo, la celda Width de una forma puede contener una fórmula que calcule el ancho de la forma según el valor de la celda Height, de modo que cuando el usuario cambie el alto de la fórmula, el ancho variará en la proporción adecuada.
ms.openlocfilehash: 54c7fd69e2ddaa9350996e2d8c921958a04e34ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821495"
---
# <a name="about-cell-references"></a>Referencias a celdas

Puede crear dependencias entre fórmulas por medio de las referencias a celdas de ShapeSheet. Las referencias a celdas le dan la posibilidad de calcular el valor de una celda basándose en el valor de otra. Por ejemplo, la celda Width de una forma puede contener una fórmula que calcule el ancho de la forma según el valor de la celda Height, de modo que cuando el usuario cambie el alto de la fórmula, el ancho variará en la proporción adecuada.
  
En la fórmula de una celda puede incluir una referencia a otra celda de la misma forma o de otro objeto, como un documento o una página; Microsoft Visio calculará el valor de una celda basándose en el valor de otra.
  
## <a name="what-cell-references-can-include"></a>Pueden incluir las referencias qué celdas

Referencias a celdas pueden incluir nombres o identificadores de forma (ID). Siempre puede hacer referencia a cualquier forma de la página por su identificador, si la forma se denomina o no. Si no se ha asignado nombre a una forma, su nombre predeterminado es hoja. *i* , donde *i* es el identificador de la forma. El identificador se asigna cuando la forma se crea y no cambia a menos que se mueve la forma a otra página o documento. Si más de una forma en una página con el mismo nombre, debe incluir el identificador asignado. 
  
## <a name="cell-reference-syntax-and-examples"></a>Ejemplos y la sintaxis de la referencia de celda

La sintaxis utilizada y la posibilidad de hacer referencia a una forma por su nombre dependen de la relación entre los dos objetos. En general se aplican las siguientes reglas:
  
- Si una forma está en el mismo nivel que aquélla cuya fórmula está modificando, puede hacer referencia a ella por su nombre. Si la forma del mismo nivel es un grupo, puede hacer referencia por el nombre al grupo, pero no a sus miembros. No es posible hacer referencia por nombre al objeto primario de una forma ni a otros objetos de su nivel.
    
- Puede utilizar la sintaxis Sheet.Id para hacer referencia a cualquier forma de la página, tanto si pertenece a un grupo como si es el objeto primario de otra forma.
    
- Los nombres que contienen caracteres no estándar deben encerrarse entre comillas simples. Los caracteres de comillas simples incluidos en nombres no estándar deben ir precedidos de una comilla simple.
    
|**Para hacer referencia a una celda de**|**Use esta sintaxis**|**Ejemplo**|
|:-----|:-----|:-----|
|La misma forma  <br/> | NombreDeCelda  <br/> | Ancho  <br/> |
| Una forma, grupo o guía  <br/> | ¡NombreDeForma! NombreDeCelda  <br/> | ¡Estrella! Ángulo  <br/> |
| Una forma, grupo o guía en las que más de una forma en el mismo nivel tiene el mismo nombre  <br/> | ¡Shapename.ID! NombreDeCelda  <br/> | ¡Executive.2! Alto  <br/> |
| Una columna con nombre con filas indizadas  <br/> | Section.Column[index]  <br/> | Char.Font[3]  <br/> |
| Una columna sin nombre con filas indizadas  <br/> | Section.ColumnIndex  <br/> | Scratch.A5  <br/> |
| Cualquier forma, página, patrón o estilo  <br/> | ¡Sheet.ID! NombreDeCelda  <br/> | ¡Sheet.8! FillForegnd  <br/> |
| Un patrón  <br/> | ¡Masters [MasterName]! ¡SheetName! ReferenciaDeCelda  <br/> | ¡Masters [engranaje]! ¡Eje! Geometry1.X1  <br/> |
| La página o página maestra en la que se encuentra el objeto  <br/> | ¡Página! ReferenciaDeCelda  <br/> | ¡Página! User.Vanishing_Point  <br/> |
| Otra página del documento  <br/> | ¡Páginas [PageName]! ¡SheetName! ReferenciaDeCelda  <br/> | ¡Páginas [página-3]! ¡Hoja.4! Celda BeginX  <br/> |
| Un estilo  <br/> | ¡Estilos! ¡SheetName! ReferenciaDeCelda  <br/> | ¡Estilos! ¡Administrador de! LineColor  <br/> |
| El documento  <br/> | ¡TheDoc! ReferenciaDeCelda  <br/> | ¡TheDoc! PreviewQuality  <br/> |
| Una forma, página, patrón, documento o estilo con un nombre no estándar.  <br/> | 'Sheetname'! NombreDeCelda  <br/> | ' 1-D'! LineColor  <br/> |
   

