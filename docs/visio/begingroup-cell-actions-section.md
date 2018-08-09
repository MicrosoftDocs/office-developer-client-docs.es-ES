---
title: Celda BeginGroup (Sección de acciones)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Indica si se inserta un separador en el menú encima de esta acción.
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821556"
---
# <a name="begingroup-cell-actions-section"></a>Celda BeginGroup (sección Acciones)

Indica si se inserta un separador en el menú encima de esta acción. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |
          Se inserta un separador en el menú encima de esta acción. 
  <br/> |
|FALSE  <br/> |
          No se inserta un separador en el menú encima de esta acción (valor predeterminado).
  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda BeginGroup por su nombre desde otra fórmula, o desde un programa mediante la propiedad
 **CellsU**, utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |Acciones. *nombre*. BeginGroup donde acciones. *nombre* es el nombre de la fila de acciones  <br/> |
   
Para obtener una referencia desde un programa a la celda BeginGroup por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionAction** <br/> |
|Índice de fila:  <br/> |**visRowAction** +  *i* donde *i* = 0, 1, 2...  <br/> |
|Índice de celda:  <br/> |**visActionBeginGroup** <br/> |
   

