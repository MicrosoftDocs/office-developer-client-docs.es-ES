---
title: Celda Case (Sección de caracteres)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Determina el uso de mayúsculas y minúsculas en el texto de una forma. Las opciones de todas las letras en mayúsculas (1) y mayúsculas iniciales (2) no cambian la apariencia del texto escrito totalmente en mayúsculas. El texto debe estar en minúsculas para que estas opciones surtan efecto.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434350"
---
# <a name="case-cell-character-section"></a>Celda Case (Sección de caracteres)

Determina el uso de mayúsculas y minúsculas en el texto de una forma. Las opciones de todas las letras en mayúsculas (1) y mayúsculas iniciales (2) no cambian la apariencia del texto escrito totalmente en mayúsculas. El texto debe estar en minúsculas para que estas opciones surtan efecto.
  
|**Valor**|**Descripción**|**Constante de automatización**|
|:-----|:-----|:-----|
| comprendi  <br/> | Uso normal de mayúsculas y minúsculas  <br/> |**visCaseNormal** <br/> |
| 1  <br/> | Todo en mayúsculas  <br/> |**visCaseAllCaps** <br/> |
| segundo  <br/> | Sólo las letras iniciales en mayúsculas  <br/> |**visCaseInitialCaps** <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda Case por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | Char. Case [ *i* ] donde *i* = <1>, 2, 3,...  <br/> |
   
Para obtener una referencia desde un programa a la celda Case por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionCharacter** <br/> |
| Índice de fila:  <br/> |**visRowCharacter** +  *i* donde *i* = 0, 1, 2,...  <br/> |
| Índice de celda:  <br/> |**visCharacterCase** <br/> |
   

