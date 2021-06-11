---
title: Celda QuickStyleVariation (sección Estilo rápido)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina si se invalidan las fórmulas y los valores del color de relleno, línea y texto (o una combinación de esas propiedades) mediante colores que contrastan con el fondo del diagrama. El valor es un OR bit a bit de 0, 1, 2, 4 y 8.
ms.openlocfilehash: 736e2287c00c24774ef8b677613235d642697f4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433797"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>Celda QuickStyleVariation (sección Estilo rápido)

Determina si se invalidan las fórmulas y los valores del color de relleno, línea y texto (o una combinación de esas propiedades) mediante colores que contrastan con el fondo del diagrama. El valor es un OR bit a bit de 0, 1, 2, 4 y 8.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |No modifique el texto, la línea o el color de relleno de una forma (o cualquier combinación de esas propiedades) para que permanezca visible con el color de fondo de un tema.  <br/> |
|1  <br/> |No modifique el texto, la línea o el color de relleno de una forma (o cualquier combinación de esas propiedades) para que permanezca visible con el color de fondo de un tema.  <br/> |
|2  <br/> |Altere el color de texto de una forma, si es necesario, para que permanezca visible en el color de fondo de un tema.  <br/> |
|4   <br/> |Altere el color de línea de una forma, si es necesario, para que permanezca visible en el color de fondo de un tema.  <br/> |
|8   <br/> |Altere el color de relleno de una forma, si es necesario, para que permanezca visible en el color de fondo de un tema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Use la celda QuickStyleVariation para garantizar la visibilidad en texto o líneas cuando están fuera de cualquier geometría de forma visible (por ejemplo, en una forma cuyo cuadro de texto está debajo de la parte inferior de la forma, como las de diagramas de red). El valor predeterminado de la celda es 0, lo que significa que su comportamiento está inactivo. Cualquier otro valor desencadena el comportamiento de la celda.
  
El valor QuickStyleVariation invalida el valor producido por la función THEMEVAL cuando reside en las celdas Color (sección Carácter), FillForegnd o LineColor (o producidas por referencias directas a estas tres propiedades mediante THEMEVAL("CharacterColor"), THEMEVAL("FillColor") y THEMEVAL("LineColor")).
  
Para obtener una referencia a la **celda QuickStyleVariation** por su nombre desde otra fórmula, obteniendo el valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |QuickStyleVariation  <br/> |
   
Para obtener una referencia desde un programa a la **celda QuickStyleVariation** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
|Índice de celda:  <br/> |**visQuickStyleVariation** <br/> |
   

