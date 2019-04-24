---
title: Celda Type (Sección de campos de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1060
localization_priority: Normal
ms.assetid: 69d64520-9a47-07ca-09c7-d1e5da620348
description: Especifica un tipo de datos para el valor del campo de texto.
ms.openlocfilehash: 91a2d60133d9a39e152656558f168742a5409883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358929"
---
# <a name="type-cell-text-fields-section"></a>Celda Type (Sección de campos de texto)

Especifica un tipo de datos para el valor del campo de texto.
  
|**Value**|**Descripción**|
|:-----|:-----|
|comprendi  <br/> |Cadena.  <br/> |
|segundo  <br/> |Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.  <br/> |
|2,5  <br/> |Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.  <br/> |
|6,5  <br/> |Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.  <br/> |
|0,7  <br/> |Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de esta celda mediante el cuadro de diálogo **campo** (con una forma seleccionada, en la ficha **Insertar** , en el grupo **texto** , haga clic en **campo** ). 
  
Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Fields. Type [ *i* ] donde *i* = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Type por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionTextField** <br/> |
|Índice de fila:  <br/> |**visRowField** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visFieldType** <br/> |
   

