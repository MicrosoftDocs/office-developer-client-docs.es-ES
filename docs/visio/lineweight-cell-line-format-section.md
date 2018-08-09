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
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822470"
---
# <a name="lineweight-cell-line-format-section"></a>Celda LineWeight (sección Formato de línea)

Determina el grosor de línea de una forma. Para establecer el grosor de línea, escriba un número con una unidad de medida válida.
  
## <a name="remarks"></a>Observaciones

También puede establecer este valor de LineWeight en el cuadro de diálogo **Línea** (haga clic en la pestaña **Inicio** del grupo **Forma**, haga clic en **Línea**, vaya a **Grosor** y, a continuación, haga clic en **Más líneas**).
  
Si no se especifica la unidad de medida, se utiliza la unidad de medida para el texto especificado en el cuadro de diálogo **Opciones de Visio** (haga clic en la pestaña **archivo** y, a continuación, haga clic en **Opciones**). Grosor de línea es independiente de la escala del dibujo. Si se cambia la escala del dibujo, el grosor de línea sigue siendo la misma. 
  
Para obtener una referencia a la celda LineWeight por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Grosor de línea  <br/> |
   
Para obtener una referencia desde un programa a la celda LineWeight por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLine** <br/> |
| Índice de celda:  <br/> |**visLineWeight** <br/> |
   

