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
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405677"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>Celda LocalizeMerge (Sección de varios)

Determina si las formas se traducen al copiarlas de un documento a otro.
  
|**Valor**|**Descripción**|
|:-----|:-----|
| TRUE  <br/> | Traduce una forma al idioma del documento de destino.  <br/> |
| FALSE  <br/> | No localice una forma en función del idioma del documento de destino (valor predeterminado).  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda LocalizeMerge por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LocalizeMerge  <br/> |
   
Para obtener una referencia desde un programa a la celda LocalizeMerge por su índice
, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowMisc** <br/> |
| Índice de celda:  <br/> |**visObjLocalizeMerge** <br/> |
   

