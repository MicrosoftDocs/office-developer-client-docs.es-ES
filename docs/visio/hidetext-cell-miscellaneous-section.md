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
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425487"
---
# <a name="hidetext-cell-miscellaneous-section"></a>Celda HideText (Sección de varios)

Oculta el texto en una forma. Puede ver el texto, editar las propiedades y aplicar diversos estilos al texto en el bloque de texto, aunque los cambios no aparezcan hasta que restablezca HideText a FALSE (0).
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | El texto se encuentra oculto y no se imprime.  <br/> |
| FALSE  <br/> | El texto no se encuentra oculto.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda HideText por su nombre desde otra fórmula, o desde un programa mediante la **propiedad CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | HideText  <br/> |
   
Para obtener una referencia desde un programa a la celda HideText por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visHideText** <br/> |
   

