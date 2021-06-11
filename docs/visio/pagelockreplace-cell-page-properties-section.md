---
title: Celda PageLockReplace (sección Propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica si el botón Reemplazar forma debe deshabilitarse para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433104"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Celda PageLockReplace (sección Propiedades de página)

Indica si el botón **Reemplazar forma** debe deshabilitarse para esta página. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El **botón Cambiar forma** se atenua cuando esta página está activa.  <br/> |
|FALSE  <br/> |Esta **página no** deshabilita el botón Cambiar forma. Es posible que el botón todavía esté atenuado si: **DocLockReplace** en **DocumentSheet** está establecido en **TRUE**; la **celda LockReplace** de la forma seleccionada se establece en **TRUE**.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **PageLockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un **elemento Cell** o desde un programa mediante la propiedad **CellsU,** use: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLockReplace  <br/> |
   
Para obtener una referencia desde un programa a la celda **PageLockReplace** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageLockReplace** <br/> |
   

