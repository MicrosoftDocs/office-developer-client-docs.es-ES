---
title: Celda PageLockReplace (sección de propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica si el botón reemplazar forma debe estar deshabilitado para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339483"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Celda PageLockReplace (sección de propiedades de página)

Indica si el botón **reemplazar forma** debe estar deshabilitado para esta página. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El botón **Cambiar forma** aparece atenuado cuando esta página está activa.  <br/> |
|FALSE  <br/> |Esta página no ha deshabilitado el botón **Cambiar forma** . El botón todavía puede estar atenuado si: el **DocLockReplace** en **DocumentSheet** se establece en **true**; la celda **LockReplace** de la forma seleccionada se establece en **true**.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **PageLockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLockReplace  <br/> |
   
Para obtener una referencia desde un programa a la celda **PageLockReplace** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageLockReplace** <br/> |
   

