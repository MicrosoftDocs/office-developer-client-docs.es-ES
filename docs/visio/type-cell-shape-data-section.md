---
title: Celda Type (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1055
localization_priority: Normal
ms.assetid: 1e24a906-83ce-32d2-5d7b-ba6dd6eea2d3
description: Especifica un tipo de datos para el valor de los datos de formas.
ms.openlocfilehash: c2d38b521a8597a4582a4145ad808b0c0e26ff0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406251"
---
# <a name="type-cell-shape-data-section"></a>Celda Type (Sección de datos de formas)

Especifica un tipo de datos para el valor de los datos de formas.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Cadena. Éste es el valor predeterminado.  <br/> |**visPropTypeString** <br/> |
|1  <br/> |Lista fija. Muestra los elementos de la lista en un cuadro combinado desplegable en el cuadro de diálogo **Definir datos de formas**. Especifique los elementos de la lista en la celda Format. Los usuarios solo pueden seleccionar un elemento de la lista.<br/> |**visPropTypeListFix** <br/> |
|segundo  <br/> |Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |Booleano. Muestra FALSE (falso) y TRUE (verdadero) como elementos que los usuarios pueden seleccionar en un cuadro de lista desplegable en el cuadro de diálogo **Definir datos de formas**.<br/> |**visPropTypeBool** <br/> |
|4   <br/> |Lista variable. Muestra los elementos de la lista en un cuadro combinado desplegable en el cuadro de diálogo **Definir datos de formas**. Especifique los elementos de la lista en la celda Format. Los usuarios pueden seleccionar un elemento de la lista o especificar uno nuevo que se agrega a la lista actual en la celda Format.<br/> |**visPropTypeListVar** <br/> |
|5   <br/> |Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeDate** <br/> |
|6   <br/> |Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeDuration** <br/> |
|7   <br/> |Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Polyprop. *Nombre* . Tipo donde prop.  *Name* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Type por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionProp** <br/> |
|Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCustPropsType** <br/> |
   

