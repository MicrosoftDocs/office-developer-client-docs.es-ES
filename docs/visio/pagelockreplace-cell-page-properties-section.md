---
title: Celda PageLockReplace (sección Propiedades de página)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica si se debe deshabilitar el botón Reemplazar forma para esta página.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822718"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Celda PageLockReplace (sección Propiedades de página)

Indica si se debe deshabilitar el botón **Reemplazar forma** para esta página. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |El botón **Cambiar forma** está atenuado cuando esta página está activa.  <br/> |
|FALSE  <br/> |El botón **Cambiar forma** no está deshabilitado por esta página. El botón es posible que aún se atenuada if: el **DocLockReplace** en el **DocumentSheet** está establecida en **TRUE**; la celda **LockReplace** para la forma seleccionada se establece en **TRUE**.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **PageLockReplace** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | PageLockReplace  <br/> |
   
Para obtener una referencia a la celda **PageLockReplace** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowPage** <br/> |
| Índice de celda:  <br/> |**visPageLockReplace** <br/> |
   

