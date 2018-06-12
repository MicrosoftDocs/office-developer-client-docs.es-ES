---
title: Celda HideText (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Oculta el texto en una forma. Puede ver el texto, editar las propiedades y aplicar diversos estilos al texto en el bloque de texto, aunque los cambios no aparezcan hasta que restablezca HideText a FALSE (0).
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822290"
---
# <a name="hidetext-cell-miscellaneous-section"></a>Celda HideText (sección de varios)

Oculta el texto en una forma. Puede ver el texto, editar las propiedades y aplicar diversos estilos al texto en el bloque de texto, aunque los cambios no aparezcan hasta que restablezca HideText a FALSE (0).
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El texto se encuentra oculto y no se imprime.  <br/> |
| FALSE  <br/> | El texto no se encuentra oculto.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda HideText por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | HideText  <br/> |
   
Para obtener una referencia a la celda HideText por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visHideText** <br/> |
   

