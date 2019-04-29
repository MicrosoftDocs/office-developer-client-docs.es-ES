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
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436331"
---
# <a name="menu-cell-actions-section"></a>Celda Menu (sección de acciones)

Define el nombre de un elemento de menú que aparece en un menú contextual o de etiqueta de acción para una forma o una página. 
  
> [!NOTE]
> En versiones anteriores de Microsoft Visio, las etiquetas de acción se denominaban etiquetas inteligentes. 
  
## <a name="remarks"></a>Comentarios

Para insertar un separador en el menú situado encima de este elemento, utilice la celda BeginGroup. Para mostrar el comando en la parte inferior del menú, coloque un carácter de porcentaje (%) como prefijo del nombre.
  
Para obtener una referencia a la celda menu por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Actividades. *nombre* . Acciones Menudonde.  *nombre* es el nombre de la fila de acciones.  <br/> |
   
Para obtener una referencia desde un programa a la celda Menu por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde i = 0, 1, 2,...  <br/> |
|Índice de celda:  <br/> |**visActionMenu** <br/> |
   

