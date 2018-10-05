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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385483"
---
# <a name="buttonface-cell-action-tags-section"></a>Celda ButtonFace (sección Etiquetas de acción)

Contiene el id. de la imagen de botón que aparece en el botón de etiqueta de acción. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

La cadena de la celda ButtonFace representa el id. de una imagen de botón de Microsoft Office. Si el valor es 0 (cero) o si no hay ningún valor, se aplica la forma predeterminada del botón de información "i" estándar de etiquetas de acción ![Botón de información "i" de etiquetas de acción estándar](media/InfoPS_ZA10180114.gif).
  
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
   

