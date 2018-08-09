---
title: Celda ButtonFace (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821691"
---
# <a name="buttonface-cell-actions-section"></a>Celda ButtonFace (sección Acciones)

Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Observaciones

La cadena de la celda ButtonFace representa el identificador de una imagen de botón de Microsoft Office. Si el valor es cero (0) o si no hay ningún valor, no aparecerá ningún icono. 
  
Los identificadores que pueden usarse en la celda ButtonFace son los mismos que los identificadores que se utiliza con la propiedad **FaceID** de un objeto **CommandBarButton** . Para obtener más detalles acerca de estos identificadores, busque "trabajar con imágenes de botón de barra de comandos" en MSDN. 
  
Para obtener una referencia a la celda ButtonFace por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |**Acciones**.  *nombre* . **ButtonFace** donde **acciones**.  *nombre* es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia desde un programa a la celda ButtonFace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde **i** = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionButtonFace** <br/> |
   

