---
title: Celda ButtonFace (sección de etiquetas de acción)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción.
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821692"
---
# <a name="buttonface-cell-action-tags-section"></a>Celda ButtonFace (sección Etiquetas de acción)

Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

La cadena de la celda ButtonFace representa el identificador de una imagen de botón de Microsoft Office. Un valor de 0 (cero) o en blanco el valor predeterminado es el botón de información "i" de etiquetas de acción estándar ![](media/InfoPS_ZA10180114.gif).
  
Los identificadores que pueden usarse en la celda ButtonFace son los mismos que los identificadores que se utiliza con la propiedad **FaceID** de un objeto **CommandBarButton** . Para obtener más detalles acerca de estos identificadores, busque "trabajar con imágenes de botón de barra de comandos" en MSDN. 
  
Para obtener una referencia a la celda ButtonFace por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Etiquetas inteligentes.  *nombre* . ButtonFace donde SmartTags. *nombre* es el nombre de la fila de etiquetas de acción  <br/> |
   
Para obtener una referencia desde un programa a la celda ButtonFace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag** +  *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagButtonFace** <br/> |
   

