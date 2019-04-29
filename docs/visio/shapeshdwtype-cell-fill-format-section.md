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
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430262"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a>Celda ShapeShdwType (Sección de formato de relleno)

Especifica el tipo de sombra de una forma. 
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
|comprendi  <br/> |Se utilizan las opciones predeterminadas de la página (valor predeterminado)  <br/> |**visFSTPageDefault** <br/> |
|1  <br/> |Simple  <br/> |**visFSTSimple** <br/> |
|segundo  <br/> |Oblicua  <br/> |**visFSTOblique** <br/> |
   
## <a name="remarks"></a>Comentarios

Use esta celda para aplicar una sombra de forma diferente de la predeterminada para la página (el tipo de sombra predeterminado de la página se define en la celda ShdwType de la sección Propiedades de página).
  
Las sombras simples se describen en la interfaz de usuario como sombras de desplazamiento. Una sombra simple proporciona un efecto de sombra sobre un plano paralelo situado detrás de la forma. Las sombras oblicuas se describen en la interfaz de usuario como sombras oblicuas y proporcionan un efecto de sombra que se proyecta sobre un plano perpendicular a la forma. 
  
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
   

