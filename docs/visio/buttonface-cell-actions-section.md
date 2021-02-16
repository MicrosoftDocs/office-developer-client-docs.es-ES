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
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407378"
---
# <a name="buttonface-cell-actions-section"></a>Celda ButtonFace (sección de acciones)

Identifica el icono que aparece junto a un elemento en un menú contextual o de etiquetas de acción.
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

La cadena de la celda ButtonFace representa el identificador de una imagen de botón de Microsoft Office. Si el valor es cero (0) o si no hay ningún valor, no aparecerá ningún icono. 
  
Los Id. que se pueden utilizar en la celda ButtonFace son los mismos que los utilizados con la propiedad **FaceID** de un objeto **CommandBarButton**. Para obtener más información sobre estos IDs, busque "trabajar con imágenes de botón de barra de comandos" en MSDN. 
  
Para obtener una referencia a la celda ButtonFace por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, use: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |**Acciones**.  *nombre*  . **ButtonFace**         donde **Actions**.  *es*  el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia desde un programa a la celda ButtonFace por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction**  +   *i* donde **i** = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionButtonFace** <br/> |
   

