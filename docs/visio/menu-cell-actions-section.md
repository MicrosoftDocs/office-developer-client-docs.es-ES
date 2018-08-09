---
title: Celda Menu (sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página.
ms.openlocfilehash: 195af94c4c36bb3c29a4fadab3c68f8334742952
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822680"
---
# <a name="menu-cell-actions-section"></a>Celda Menu (sección Acciones)

Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Observaciones

Para insertar un separador en el menú situado encima de este elemento, utilice la celda BeginGroup. Para mostrar el comando en la parte inferior del menú, coloque un carácter de porcentaje (%) como prefijo del nombre.
  
Para obtener una referencia a la celda Menu por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Acciones. *nombre* . Acciones de Menuwhere.  *nombre* es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia desde un programa a la celda Menu por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visActionMenu** <br/> |
   

