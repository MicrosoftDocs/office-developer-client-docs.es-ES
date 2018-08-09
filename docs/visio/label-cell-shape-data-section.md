---
title: Celda Label (Sección de datos de formas)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Especifica la etiqueta que se muestra a los usuarios en la ventana Datos de formas. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_).
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822388"
---
# <a name="label-cell-shape-data-section"></a>Celda Label (sección Datos de formas)

Especifica la etiqueta que se muestra a los usuarios en la ventana **Datos de formas**. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_). 
  
## <a name="remarks"></a>Comentarios

La aplicación encierra automáticamente la cadena Label entre comillas en la celda, aunque las comillas no se muestran en la ventana **Datos de formas**. 
  
Si no encuentra ningún texto de etiqueta, Visio muestra el nombre de fila (Prop.Row) en la ventana **Datos de formas**. 
  
Para obtener una referencia a la celda Label por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |De propiedades. *Nombre* . Etiqueta de propiedades donde.  *Nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Label por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionProp** <br/> |
|Índice de fila:  <br/> |**visRowProp** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCustPropsLabel** <br/> |
   

