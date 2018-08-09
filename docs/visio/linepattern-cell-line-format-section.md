---
title: Celda LinePattern (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: Determina la trama de línea de la forma. El valor especificado en la celda LinePattern es un número que actúa como índice en una colección de tramas de línea.
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822462"
---
# <a name="linepattern-cell-line-format-section"></a>Celda LinePattern (sección Formato de línea)

Determina la trama de línea de la forma. El valor especificado en la celda LinePattern es un número que actúa como índice en una colección de tramas de línea.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0  <br/> |Sin trama de línea  <br/> |
|1  <br/> |Sólido  <br/> |
|2 - 23  <br/> |Varias tramas de línea  <br/> |
   
## <a name="remarks"></a>Observaciones

Puede ver la colección de tramas de línea en el cuadro de diálogo **Línea** (en la ficha **Inicio**, en el grupo **Forma**, haga clic en **Línea**, seleccione **Guiones** y, a continuación, haga clic en **Más líneas**).
  
Puede especificar una trama de línea personalizada si utiliza la función USE en esta celda.
  
Para obtener una referencia a la celda LinePattern por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LinePattern  <br/> |
   
Para obtener una referencia desde un programa a la celda LinePattern por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLine** <br/> |
|Índice de celda:  <br/> |**visLinePattern** <br/> |
   

