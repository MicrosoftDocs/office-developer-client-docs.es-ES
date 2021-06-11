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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407987"
---
# <a name="type-cell-text-fields-section"></a>Celda Type (Sección de campos de texto)

Especifica un tipo de datos para el valor del campo de texto.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Cadena.  <br/> |
|2  <br/> |Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.  <br/> |
|5   <br/> |Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.  <br/> |
|6   <br/> |Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.  <br/> |
|7   <br/> |Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.  <br/> |
   
## <a name="remarks"></a>Comentarios

También puede establecer el valor de  esta celda mediante el cuadro  de diálogo Campo  (con una forma seleccionada, en la ficha Insertar, en el grupo Texto, haga clic en **Campo** ). 
  
Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Fields.Type[ *i*  ] donde  *i*  = <1>, 2, 3...  <br/> |
   
Para obtener una referencia desde un programa a la celda Type por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionTextField** <br/> |
|Índice de fila:  <br/> |**visRowField**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visFieldType** <br/> |
   

