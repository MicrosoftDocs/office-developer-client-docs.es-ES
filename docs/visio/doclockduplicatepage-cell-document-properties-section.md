---
title: Celda DocLockDuplicatePage (sección Propiedades del documento)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina si se pueden duplicar las páginas del documento, como un valor Boolean.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822001"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>Celda DocLockDuplicatePage (sección Propiedades del documento)

Determina si se pueden duplicar las páginas del documento, como un valor Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplicar** en el menú contextual de la página y el método de automatización **Page.Duplicate** están deshabilitados.  <br/> |
|FALSE  <br/> |Puede duplicar la página.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **DocLockDuplicatePage** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | DocLockDuplicatePage  <br/> |
   
Para obtener una referencia a la celda **DocLockDuplicatePage** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowDoc** <br/> |
| Índice de celda:  <br/> |**visDocLockDuplicatePage** <br/> |
   

