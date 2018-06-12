---
title: Celda Transparency (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Determina el nivel de transparencia de color de un intervalo de texto de una forma.
ms.openlocfilehash: 5914a061b1bba2173b338544b05abda8780ff164
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823426"
---
# <a name="transparency-cell-character-section"></a>Celda Transparency (Sección de caracteres)

Determina el nivel de transparencia de color de un intervalo de texto de una forma.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0 - 100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Observaciones

Los valores se redondean al medio porcentaje más próximo. El valor 100% hace que sea totalmente transparente. Aunque una forma con texto totalmente transparente y otra sin texto tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página se producirá como si su transparencia fuera del 0%.
  
También puede establecer este valor mediante el control deslizante en la ficha **fuente** en el cuadro de diálogo **texto** (en la ficha **Inicio** , haga clic en la flecha de **fuente** ). 
  
Si la sección de caracteres contiene varias filas, la celda Transparency contiene la información de formato que se aplica a un subintervalo del texto de la forma. En caso contrario, contiene información de formato para todo el texto de la forma.
  
Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Char.ColorTrans [ *i* ] donde *i* = < 1 >, 2, 3...  <br/> |
   
Para obtener una referencia a la celda Transparency por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionCharacter** <br/> |
|Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visCharacterColorTrans** <br/> |
   

