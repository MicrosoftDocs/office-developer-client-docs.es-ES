---
title: Celda LineWeight (Sección de formato de línea)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Determina el grosor de línea de una forma. Para establecer el grosor de línea, escriba un número con una unidad de medida válida.
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412250"
---
# <a name="lineweight-cell-line-format-section"></a>Celda LineWeight (Sección de formato de línea)

Determina el grosor de línea de una forma. Para establecer el grosor de línea, escriba un número con una unidad de medida válida.
  
## <a name="remarks"></a>Comentarios

También puede establecer este valor de LineWeight en el cuadro de diálogo **Línea** (haga clic en la pestaña **Inicio** del grupo **Forma**, haga clic en **Línea**, vaya a **Grosor** y, a continuación, haga clic en **Más líneas**).
  
Si no se especifica la unidad de medida, se usa la unidad de medida  del texto especificado en el cuadro de diálogo Opciones de **Visio** (haga clic en la ficha Archivo y, a continuación, haga clic en **Opciones).** El grosor de línea no depende de la escala del dibujo. Si se cambia la escala del dibujo, el grosor de línea permanece igual. 
  
Para obtener una referencia a la celda LineWeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LineWeight  <br/> |
   
Para obtener una referencia desde un programa a la celda LineWeight por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLine** <br/> |
| Índice de celda:  <br/> |**visLineWeight** <br/> |
   

