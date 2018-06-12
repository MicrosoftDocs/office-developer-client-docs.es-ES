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
ms.openlocfilehash: 68bfa8a84adb0d46d9621e6fc5383f4b6606f542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823459"
---
# <a name="type-cell-text-fields-section"></a>Celda Type (Sección de campos de texto)

Especifica un tipo de datos para el valor del campo de texto.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Cadena.  <br/> |
|2  <br/> |Número. Incluye los valores de fecha, hora, duración y moneda, así como escalares, dimensiones y ángulos. Especifique una imagen de formato en la celda Format.  <br/> |
|5  <br/> |Valor de fecha u hora. Muestra días, meses y años; o segundos, minutos y horas; o un valor combinado de fecha y hora. Especifique una imagen de formato en la celda Format.  <br/> |
|6  <br/> |Valor de duración. Muestra el tiempo transcurrido. Especifique una imagen de formato en la celda Format.  <br/> |
|7  <br/> |Valor de moneda. Utiliza la configuración regional actual del sistema. Especifique una imagen de formato en la celda Format.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede establecer el valor de esta celda mediante el cuadro de diálogo **campo** (con una forma seleccionada, en la ficha **Insertar** , en el grupo **texto** , haga clic en **campo** ). 
  
Para obtener una referencia a la celda Type por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Fields.Type [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Type por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionTextField** <br/> |
|Índice de fila:  <br/> |**visRowField** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visFieldType** <br/> |
   

