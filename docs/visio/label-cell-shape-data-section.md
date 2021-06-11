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
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420181"
---
# <a name="label-cell-shape-data-section"></a>Celda Label (Sección de datos de formas)

Especifica la etiqueta que se muestra a los usuarios en la ventana **Datos de formas**. Una etiqueta está compuesta de caracteres alfanuméricos, incluido el carácter de subrayado (_). 
  
## <a name="remarks"></a>Comentarios

La aplicación encierra automáticamente la cadena Label entre comillas en la celda, aunque las comillas no se muestran en la ventana **Datos de formas**. 
  
Si no encuentra ningún texto de etiqueta, Visio muestra el nombre de fila (Prop.Row) en la ventana **Datos de formas**. 
  
Para obtener una referencia a la celda Label por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Prop. *Name*  . Etiqueta donde Prop.  *Name*  es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Label por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionProp** <br/> |
|Índice de fila:  <br/> |**visRowProp**  +   *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCustPropsLabel** <br/> |
   

