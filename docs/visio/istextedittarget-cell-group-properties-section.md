---
title: Celda IsTextEditTarget (Sección de propiedades de grupo)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: Determina las asignaciones de texto para un grupo.
ms.openlocfilehash: 65baf90254f6b213efea04739d8e4a66952b2856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822393"
---
# <a name="istextedittarget-cell-group-properties-section"></a>Celda IsTextEditTarget (Sección de propiedades de grupo)

Determina las asignaciones de texto para un grupo.
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El texto se agrega a la forma del grupo.  <br/> |
|FALSE  <br/> |El texto se agrega a la forma en el grupo en la parte superior del orden de apilamiento.  <br/> |
   
## <a name="remarks"></a>Observaciones

También puede establecer este valor, seleccione el grupo, hace clic en **comportamiento** en la ficha [Programador](run-in-developer-mode-display-the-developer-tab.md) y a continuación, selecciona la casilla de verificación **modificar el texto del grupo** . 
  
Los grupos creados con versiones anteriores a Visio 2000 tienen el valor predeterminado FALSE. A partir de la versión 2000 de Visio, el valor predeterminado es TRUE. 
  
Para obtener una referencia a la celda IsTextEditTarget por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Valor de IsTextEditTarget  <br/> |
   
Para obtener una referencia a la celda IsTextEditTarget por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowGroup** <br/> |
|Índice de celda:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

