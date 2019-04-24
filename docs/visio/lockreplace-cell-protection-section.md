---
title: Celda LockReplace (sección protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica si una forma puede participar en una operación de reemplazo (como una forma de destino o de reemplazo).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348226"
---
# <a name="lockreplace-cell-protection-section"></a>Celda LockReplace (sección protección)

Indica si una forma puede participar en una operación de reemplazo (como una forma de destino o de reemplazo). 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La forma no se puede reemplazar o usar como una forma de reemplazo.  <br/> En el caso de una forma en el lienzo, el botón **Cambiar forma** se deshabilita cuando se selecciona la forma.  <br/> En el caso de una forma de una galería de símbolos, la forma no aparece como una forma de reemplazo cuando se hace clic en el botón **Cambiar forma** .  <br/> |
|FALSE  <br/> |La forma se puede reemplazar o usar como una forma de reemplazo.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockReplace** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockReplace  <br/> |
   
Para obtener una referencia desde un programa a la celda **LockReplace** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockReplace** <br/> |
   

