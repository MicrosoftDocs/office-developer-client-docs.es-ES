---
title: Celda ShdwType (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indica el tipo de sombra predeterminado para una página.
ms.openlocfilehash: f1fc72484d94788ca2798760ca935c89c3e841ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424101"
---
# <a name="shdwtype-cell-page-properties-section"></a>Celda ShdwType (Sección de propiedades de página)

Indica el tipo de sombra predeterminado para una página.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblicua  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Interno  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Comentarios

 El tipo de sombra descrito en esta celda se usa siempre que la celda ShapeShdwType (el tipo de sombra de una forma individual de la página) se establece en Page Default (**visFSTPageDefault** ). 
  
Las sombras simples se describen en la interfaz de usuario como sombras de desplazamiento. Una sombra simple proporciona un efecto de sombra sobre un plano paralelo situado a cierta distancia detrás de la forma. Las sombras oblicuas se describen en la interfaz de usuario como sombras oblicuas y proporcionan un efecto de sombra que se proyecta sobre un plano perpendicular a la forma. 
  
Para consultar una lista de tipos de sombras simples y oblicuas predeterminados, vea la lista **Estilo** de la ficha **Sombras** del cuadro de diálogo **Configurar página** (en la ficha **Diseño**, haga clic en la flecha de **Configurar página**). 
  
Para obtener una referencia a la celda ShdwType por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | ShdwType  <br/> |
   
Para obtener una referencia desde un programa a la celda ShapeShdwOffsetX por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageShdwType** <br/> |
   

