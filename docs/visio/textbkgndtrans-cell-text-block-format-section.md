---
title: Celda TextBkgndTrans (Sección de formato del bloque de texto)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Determina el nivel de transparencia del color de fondo del bloque de texto de la forma.
ms.openlocfilehash: d9fee430cb2ccd19e8d6069e7561a8fef409a62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823382"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a>Celda TextBkgndTrans (sección Formato del bloque de texto)

Determina el nivel de transparencia del color de fondo del bloque de texto de la forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|
          0 -100
  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Observaciones

Los valores se redondean al medio porcentaje más próximo. El valor 100% hace que sea totalmente transparente. Aunque una forma con fondo de texto totalmente transparente y otra sin fondo de texto tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del 0%.
  
Para establecer este valor, también puede usar el control deslizante en la ficha **Fuente** del cuadro de diálogo **Texto** (en la ficha **Inicio**, haga clic en la flecha de **Fuente**). 
  
Para obtener una referencia a la celda TextBkgndTrans por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |TextBkgndTrans  <br/> |
   
Para obtener una referencia desde un programa a la celda TextBkgndTrans por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowText** <br/> |
|Índice de celda:  <br/> |**visTxtBlkBkgndTrans** <br/> |
   

