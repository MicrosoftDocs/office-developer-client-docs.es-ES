---
title: Celda LocalizeMerge (Sección de varios)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Determina si las formas se traducen al copiarlas de un documento a otro.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822484"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>Celda LocalizeMerge (Sección de varios)

Determina si las formas se traducen al copiarlas de un documento a otro.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Traduce una forma al idioma del documento de destino.  <br/> |
| FALSE  <br/> | No traduce una forma en función del idioma del documento de destino (predeterminado).  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda LocalizeMerge por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LocalizeMerge  <br/> |
   
Para obtener una referencia a la celda LocalizeMerge por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visObjLocalizeMerge** <br/> |
   

