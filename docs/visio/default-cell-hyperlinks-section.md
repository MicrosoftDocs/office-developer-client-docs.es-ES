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
ms.openlocfilehash: 9991bd0e241c5dfd4fda65aeff8b6cc203ad3458
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434357"
---
# <a name="default-cell-hyperlinks-section"></a>Celda Default (Sección de hipervínculos)

Determina el hipervínculo predeterminado de una forma o página. Asigne a esta celda el valor TRUE para establecer un hipervínculo como predeterminado.
  
## <a name="remarks"></a>Comentarios

Para establecer el hipervínculo predeterminado, también puede seleccionar una forma, hacer clic en **Hipervínculos** en el menú **Insertar**, seleccionar un hipervínculo y, a continuación, hacer clic en **Predeterminado**. El hipervínculo predeterminado aparecerá en negrita.
  
Para obtener una referencia a la celda Default por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Hipervínculo. *Nombre* . Valor predeterminado donde HYPERLINK. *Name* es el nombre de la fila  <br/> |
   
Para obtener una referencia desde un programa a la celda Default por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionHyperlink** <br/> |
|Índice de fila:  <br/> |**visRow1stHyperlink** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visHLinkDefault** <br/> |
   

