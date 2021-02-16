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
ms.openlocfilehash: e74b3281d894cebd8491112181198d427f0d337f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337544"
---
# <a name="buttonface-cell-action-tags-section"></a>Celda ButtonFace (sección de etiquetas de acción)

Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

La cadena de la celda ButtonFace representa el id. de una imagen de botón de Microsoft Office. El valor predeterminado es 0 (cero) o en blanco para el botón de información de la etiqueta de acción estándar "i". ![Botón de información de etiqueta de acción estándar "i"](media/InfoPS_ZA10180114.gif).
  
Los Id. que se pueden utilizar en la celda ButtonFace son los mismos que los utilizados con la propiedad **FaceID** de un objeto **CommandBarButton**. Para obtener más información sobre estos IDs, busque "trabajar con imágenes de botón de barra de comandos" en MSDN. 
  
Para obtener una referencia a la celda ButtonFace por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | SmartTags.  *nombre*  . ButtonFace donde SmartTags. *es*  el nombre de la fila de etiqueta de acción  <br/> |
   
Para obtener una referencia desde un programa a la celda ButtonFace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionSmartTag** <br/> |
| Índice de fila:  <br/> |**visRowSmartTag**  +   *i* donde *i* = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visSmartTagButtonFace** <br/> |
   

