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
ms.openlocfilehash: e5471dcc1ed487a5992779f1faa4763887bebb2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823458"
---
# <a name="type-cell-shape-data-section"></a>Celda Type (Sección de datos de formas)

Especifica un tipo de datos para el valor de los datos de formas.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Cadena. Éste es el valor predeterminado.  <br/> |**visPropTypeString** <br/> |
|1  <br/> |Lista fija. Muestra los elementos de lista combinado de la lista desplegable de cuadro en el cuadro de diálogo **Definir datos de formas** . Especifique los elementos de lista en la celda Format. Los usuarios pueden seleccionar un solo elemento de la lista.  <br/> |**visPropTypeListFix** <br/> |
|2  <br/> |Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeNumber** <br/> |
|3  <br/> |Valor booleano. Muestra Falso y verdadero como elementos que los usuarios pueden seleccionar en un cuadro de lista desplegable en el cuadro de diálogo **Definir datos de formas** .  <br/> |**visPropTypeBool** <br/> |
|4  <br/> |Lista de variables. Muestra los elementos de lista combinado de la lista desplegable de cuadro en el cuadro de diálogo **Definir datos de formas** . Especifique los elementos de lista en la celda Format. Los usuarios pueden seleccionar un elemento de lista o escriba un nuevo elemento que se agrega a la lista actual en la celda Format.  <br/> |**visPropTypeListVar** <br/> |
|5  <br/> |Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeDate** <br/> |
|6  <br/> |Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeDuration** <br/> |
|7  <br/> |Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.  <br/> |**visPropTypeCurrency** <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |De propiedades. *Nombre* . Tipo de propiedades donde.  *Nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia a la celda Type por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionProp** <br/> |
|Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCustPropsType** <br/> |
   

