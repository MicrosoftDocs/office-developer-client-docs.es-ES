---
title: Celda Transparency (Sección de propiedades de la imagen)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Determina el grado de transparencia del color de una capa.
ms.openlocfilehash: defe5307e57c433fcf85a4132939d08cb1ddec77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405838"
---
# <a name="transparency-cell-image-properties-section"></a>Celda Transparency (sección de propiedades de la imagen)

Determina el grado de transparencia del color de una capa.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0 -100  <br/> |Representa el porcentaje de transparencia. El valor predeterminado es 0% (totalmente opaco).  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores se redondean al medio porcentaje más próximo. El valor 100% es totalmente transparente. Aunque una capa con un color totalmente transparente y otra sin color tienen la misma apariencia en la página de dibujo, la interacción con los demás objetos de la página es la misma que si su transparencia fuera del 0%. Para establecer este valor, también puede usar el control deslizante del cuadro de diálogo **Propiedades de las capas** (en la ficha **Inicio**, en el grupo **Edición**, haga clic en **Capas** y, a continuación, en **Propiedades de las capas**).
  
Para obtener una referencia a la celda Transparency por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Transparencia  <br/> |
   
Para obtener una referencia desde un programa a la celda Transparency por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowImage** <br/> |
|Índice de celda:  <br/> |**visImageTransparency** <br/> |
   

