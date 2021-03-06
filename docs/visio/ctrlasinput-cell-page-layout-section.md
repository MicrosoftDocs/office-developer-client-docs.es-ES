---
title: Celda CtrlAsInput (Sección de diseño de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: Determina qué forma es la principal cuando se emplean formas con controladores. Esta celda establece el comportamiento de todas las formas en la página de dibujo.
ms.openlocfilehash: a530c48156043bec0cd58d79aead1a403c17ddce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422624"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>Celda CtrlAsInput (Sección de diseño de página)

Determina qué forma es la principal cuando se emplean formas con controladores. Esta celda establece el comportamiento de todas las formas en la página de dibujo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Se establece como forma principal la forma a la que está conectado el controlador.  <br/> |
| FALSE  <br/> | Valor predeterminado. Se establece como forma principal la forma que contiene el controlador.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda CtrlAsInput por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | CtrlAsInput  <br/> |
   
Para obtener una referencia desde un programa a la celda CtrlAsInput por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPageLayout** <br/> |
| Índice de celda:  <br/> |**visPLOCtrlAsInput** <br/> |
   

