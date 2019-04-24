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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342892"
---
# <a name="shdwtype-cell-page-properties-section"></a>Celda ShdwType (Sección de propiedades de página)

Indica el tipo de sombra predeterminado para una página.
  
|**Value**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| segundo  <br/> | Oblicua  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Inner  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Comentarios

 El tipo de sombra que se describe en esta celda se utiliza cuando la celda ShapeShdwType (tipo de sombra para una forma individual de la página) se establece en el valor predeterminado de página (**visFSTPageDefault** ). 
  
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
   

