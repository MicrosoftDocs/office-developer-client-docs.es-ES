---
title: Celda Prompt (Sección de celdas definidas por el usuario)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Especifica un mensaje o comentario descriptivo para la celda definida por el usuario. La aplicación incluye automáticamente el texto del mensaje entre comillas () para indicar que se trata de una cadena de texto. Si escribe un signo igual (=) y omite las comillas, puede escribir una fórmula en esta celda que evalúa la aplicación.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435729"
---
# <a name="prompt-cell-user-defined-cells-section"></a>Celda Prompt (Sección de celdas definidas por el usuario)

Especifica un mensaje o comentario descriptivo para la celda definida por el usuario. La aplicación pone automáticamente el texto del mensaje entre comillas (" ") para indicar que se trata de una cadena de texto. Si escribe un signo de igual (=) y omite las comillas, podrá escribir una fórmula en esta celda que evaluará la aplicación.
  
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Prompt por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Usuario.  *Nombre*  . Preguntar dónde usuario.  *Name*  es el nombre de fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Prompt por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionUser** <br/> |
| Índice de fila:  <br/> |**visRowUser +** *i*            donde  *i*  = 0, 1, 2...  <br/> |
| Índice de celda:  <br/> |**visUserPrompt** <br/> |
   

