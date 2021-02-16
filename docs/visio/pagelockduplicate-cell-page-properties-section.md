---
title: Celda PageLockDuplicate (Sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina si la página se puede duplicar, como un valor booleano.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425984"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Celda PageLockDuplicate (Sección de propiedades de página)

Determina si la página se puede duplicar, como un valor booleano.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Los** duplicados en el menú contextual de la página y el método de automatización **Page.Duplicate** están deshabilitados para la página.  <br/> |
|FALSE  <br/> |La página se puede duplicar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **PageLockDuplicate** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLockDuplicate  <br/> |
   
Para obtener una referencia desde un programa a la celda **PageLockDuplicate** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageLockDuplicate** <br/> |
   

