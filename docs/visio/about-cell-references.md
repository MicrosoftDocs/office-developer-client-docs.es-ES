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
ms.openlocfilehash: a92bcc560c535dc012ec5cb79db72250e78364c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409807"
---
# <a name="about-cell-references"></a>Referencias a celdas

Puede crear dependencias entre fórmulas por medio de las referencias a celdas de ShapeSheet. Las referencias a celdas le dan la posibilidad de calcular el valor de una celda basándose en el valor de otra. Por ejemplo, la celda Width de una forma puede contener una fórmula que calcule el ancho de la forma según el valor de la celda Height, de modo que cuando el usuario cambie el alto de la fórmula, el ancho variará en la proporción adecuada.
  
En la fórmula de una celda puede incluir una referencia a otra celda de la misma forma o de otro objeto, como un documento o una página; Microsoft Visio calculará el valor de una celda basándose en el valor de otra.
  
## <a name="what-cell-references-can-include"></a>Qué pueden incluir las referencias a celdas

Las referencias a celdas pueden incluir nombres o identificadores de formas. Siempre puede hacer referencia a cualquier forma de la página por su identificador, tanto si la forma tiene nombre como si no. Si no se ha asignado nombre a una forma, su nombre predeterminado será Sheet. *i* , donde *i* es el identificador de la forma. El identificador se asigna al crear la forma y no cambiará a menos que la forma se mueva a otra página o documento. Si en una página hay más de una forma con el mismo nombre, deberá especificar el identificador asignado. 
  
## <a name="cell-reference-syntax-and-examples"></a>Sintaxis y ejemplos de referencias a celdas

La sintaxis utilizada y la posibilidad de hacer referencia a una forma por su nombre dependen de la relación entre los dos objetos. En general se aplican las siguientes reglas:
  
- Si una forma está en el mismo nivel que aquélla cuya fórmula está modificando, puede hacer referencia a ella por su nombre. Si la forma del mismo nivel es un grupo, puede hacer referencia por el nombre al grupo, pero no a sus miembros. No es posible hacer referencia por nombre al objeto primario de una forma ni a otros objetos de su nivel.
    
- Puede utilizar la sintaxis Sheet.Id para hacer referencia a cualquier forma de la página, tanto si pertenece a un grupo como si es el objeto primario de otra forma.
    
- Los nombres que contienen caracteres no estándar deben encerrarse entre comillas simples. Los caracteres de comillas simples incluidos en nombres no estándar deben ir precedidos de una comilla simple.
    
|**Para hacer referencia a una celda de**|**Use esta sintaxis**|**Ejemplo**|
|:-----|:-----|:-----|
|La misma forma  <br/> | CellName  <br/> | Width  <br/> |
| Una forma, grupo o guía  <br/> | Nombredeforma! CellName  <br/> | &! Respecto  <br/> |
| Forma, grupo o guía en que hay más de una forma en el mismo nivel con el mismo nombre  <br/> | Shapename.ID! CellName  <br/> | Executive. 2 Alto  <br/> |
| Columna con nombre con filas indizadas  <br/> | Section. Column [índice]  <br/> | Char. Font [3]  <br/> |
| Columna sin nombre con filas indizadas  <br/> | Section. ColumnIndex  <br/> | Scratch. A5  <br/> |
| Cualquier forma, página, patrón o estilo  <br/> | Sheet.ID! CellName  <br/> | Sheet. 8! FillForegnd  <br/> |
| Patrón  <br/> | Patrones [MasterName]! Hoja! ReferenciaDeCelda  <br/> | Patrones [engranaje] Cambio! Geometry1. x1  <br/> |
| Página o página patrón en la que se encuentra el objeto  <br/> | La página! ReferenciaDeCelda  <br/> | La página! User. Vanishing_Point  <br/> |
| Otra página del documento  <br/> | Páginas [Nombredepágina]! Hoja! ReferenciaDeCelda  <br/> | Páginas [Page-3]! Sheet. 4! BeginX  <br/> |
| Estilo  <br/> | Stil! Hoja! ReferenciaDeCelda  <br/> | Stil! Directora! LineColor  <br/> |
| Documento  <br/> | TheDoc! ReferenciaDeCelda  <br/> | TheDoc! PreviewQuality  <br/> |
| Forma, página, patrón, documento o estilo con nombre no estándar.  <br/> | ' SheetName '. CellName  <br/> | ' 1-D '. LineColor  <br/> |
   

