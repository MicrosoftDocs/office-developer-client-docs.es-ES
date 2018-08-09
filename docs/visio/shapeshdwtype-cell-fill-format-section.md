---
title: Celda ShapeShdwType (Sección de formato de relleno)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Especifica el tipo de sombra de una forma.
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823172"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>Celda ShapeShdwType (sección Formato de relleno)

Especifica el tipo de sombra de una forma. 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|0  <br/> |Se utilizan las opciones predeterminadas de la página (valor predeterminado)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Simple  <br/> |**visFSTSimple** <br/> |
|2  <br/> |Oblicuo  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Comentarios

Use esta celda para aplicar una sombra de forma que es diferente de la predeterminada de la página (el tipo de sombra predeterminado de página se define en la celda ShdwType de la sección de propiedades de página).
  
Se describen los tipos de sombra simple como sombras de desplazamiento en la interfaz de usuario (UI). Una sombra simple proporciona un efecto de sombra sobre un plano paralelo situado detrás de la forma. Las sombras oblicuas se describen como sombras oblicuas en la interfaz de usuario y dan el efecto de la sombra se convierte en un plano perpendicular a la forma. 
  
Para obtener una lista de tipos de sombras simples y oblicuas predefinidas, vea el cuadro **Estilo** en el cuadro de diálogo **Sombra** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Sombra** y, a continuación, en **Opciones de sombra**).
  
Para obtener una referencia a la celda ShapeShdwType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |ShapeShdwType  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapeShdwType por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowFill** <br/> |
|Índice de celda:  <br/> |**visFillShdwType** <br/> |
   

