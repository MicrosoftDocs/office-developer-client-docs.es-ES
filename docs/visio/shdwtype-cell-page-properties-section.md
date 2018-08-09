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
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823221"
---
# <a name="shdwtype-cell-page-properties-section"></a>Celda ShdwType (sección Propiedades de la página)

Indica el tipo de sombra predeterminado para una página.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| 1  <br/> | Simple  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblicuo  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Interna  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Comentarios

 El tipo de sombra que se describe en esta celda se utiliza cuando la celda ShapeShdwType (tipo de sombra para una forma individual en la página) se establece el valor predeterminado de página (**visFSTPageDefault** ). 
  
Se describen los tipos de sombra simple como sombras de desplazamiento en la interfaz de usuario (UI). Una sombra simple proporciona el efecto de sombra sobre un plano paralelo situado a cierta distancia detrás de él. Las sombras oblicuas se describen como sombras oblicuas en la interfaz de usuario y dan el efecto de la sombra se convierte en un plano perpendicular a la forma. 
  
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
   

