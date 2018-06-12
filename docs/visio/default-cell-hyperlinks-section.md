---
title: Celda Default (Sección de hipervínculos)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: Determina el hipervínculo predeterminado de una forma o página. Asigne a esta celda el valor TRUE para establecer un hipervínculo como predeterminado.
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821947"
---
# <a name="default-cell-hyperlinks-section"></a>Celda Default (Sección de hipervínculos)

Determina el hipervínculo predeterminado de una forma o página. Asigne a esta celda el valor TRUE para establecer un hipervínculo como predeterminado.
  
## <a name="remarks"></a>Observaciones

También puede establecer el hipervínculo predeterminado mediante la selección de una forma, hacer clic en **hipervínculo** en la ficha **Insertar** , seleccionar un hipervínculo y, a continuación, haciendo clic en **predeterminado**. El hipervínculo predeterminado aparece en negrita.
  
Para obtener una referencia a la celda Default por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *Nombre* . Valor predeterminado donde hipervínculo. *Nombre* es el nombre de fila  <br/> |
   
Para obtener una referencia a la celda Default por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
|Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visHLinkDefault** <br/> |
   

