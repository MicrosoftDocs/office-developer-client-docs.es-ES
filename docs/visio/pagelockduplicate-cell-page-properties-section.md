---
title: Celda PageLockDuplicate (sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina si la página se puede duplicar, como un valor booleano.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283667"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Celda PageLockDuplicate (sección de propiedades de página)

Determina si la página se puede duplicar, como un valor booleano.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplicar** en el menú contextual de la página y el método de automatización **Page. duplicado** están deshabilitados para la página.  <br/> |
|FALSE  <br/> |La página se puede duplicar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **PageLockDuplicate** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLockDuplicate  <br/> |
   
Para obtener una referencia desde un programa a la celda **PageLockDuplicate** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageLockDuplicate** <br/> |
   

