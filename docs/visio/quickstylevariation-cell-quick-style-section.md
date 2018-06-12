---
title: Celda QuickStyleVariation (sección de estilos rápidos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e3b58a19-9f1a-4f2b-9fe2-45cbb7ec6898
description: Determina si se deben reemplazar las fórmulas y los valores de texto, línea y relleno color (o una combinación de esas propiedades) mediante el uso de los colores que contraste con el fondo de diagrama. El valor es una operación OR bit a bit de 0, 1, 2, 4 y 8.
ms.openlocfilehash: fe6462798b61a0713f98196974876144cf4606e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822894"
---
# <a name="quickstylevariation-cell-quick-style-section"></a>Celda QuickStyleVariation (sección de estilos rápidos)

Determina si se deben reemplazar las fórmulas y los valores de texto, línea y relleno color (o una combinación de esas propiedades) mediante el uso de los colores que contraste con el fondo de diagrama. El valor es una operación OR bit a bit de 0, 1, 2, 4 y 8.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |No modifique el texto de una forma, línea, o relleno color (o cualquier combinación de esas propiedades) para permanecer visibles contra el color de fondo especificado de un tema.  <br/> |
|1  <br/> |No modifique el texto de una forma, línea, o relleno color (o cualquier combinación de esas propiedades) para permanecer visibles contra el color de fondo especificado de un tema.  <br/> |
|2  <br/> |Modificar el color del texto de una forma, si es necesario, se mantienen visibles contra un tema al indicar el color de fondo.  <br/> |
|4  <br/> |Modificar el color de línea de una forma, si es necesario, se mantienen visibles contra un tema al indicar el color de fondo.  <br/> |
|8  <br/> |Modificar el color de relleno de una forma, si es necesario, se mantienen visibles contra un tema al indicar el color de fondo.  <br/> |
   
## <a name="remarks"></a>Notas

Utilice la celda QuickStyleVariation para garantizar la visibilidad en texto o líneas cuando están fuera de cualquier geometría de forma visible (por ejemplo, en una forma cuyo textbox está por debajo de la parte inferior de la forma, como las de diagramas de red). Valor predeterminado de la celda es 0, lo que significa que su comportamiento está inactivo. Cualquier otro valor, desencadena el comportamiento de la celda.
  
El valor de QuickStyleVariation invalida el valor generado por la función THEMEVAL cuando reside en el Color (sección de caracteres), FillForegnd o LineColor celdas (o producidos por referencias directas a estas tres propiedades por medio de THEMEVAL (" CharacterColor"), THEMEVAL("FillColor") y THEMEVAL("LineColor")).
  
Para obtener una referencia a la celda **QuickStyleVariation** por su nombre desde otra fórmula, mediante la obtención del valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |QuickStyleVariation  <br/> |
   
Para obtener una referencia a la celda **QuickStyleVariation** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowQuickStyleProperties** <br/> |
|Índice de celda:  <br/> |**visQuickStyleVariation** <br/> |
   

