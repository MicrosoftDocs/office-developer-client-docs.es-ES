---
title: Celda PageLockDuplicate (sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina si se puede duplicar la página, como un valor Boolean.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822712"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Celda PageLockDuplicate (sección de propiedades de página)

Determina si se puede duplicar la página, como un valor Boolean.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplicar** en el menú contextual de la página y el método de automatización **Page.Duplicate** están deshabilitados para la página.  <br/> |
|FALSE  <br/> |Puede duplicar la página.  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda **PageLockDuplicate** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLockDuplicate  <br/> |
   
Para obtener una referencia a la celda **PageLockDuplicate** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageLockDuplicate** <br/> |
   

