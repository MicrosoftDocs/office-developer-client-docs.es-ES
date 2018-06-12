---
title: Celda LockReplace (sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica si una forma puede participar en una operación de reemplazo (como un destino o una forma de reemplazo).
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822515"
---
# <a name="lockreplace-cell-protection-section"></a>Celda LockReplace (sección de protección)

Indica si una forma puede participar en una operación de reemplazo (como un destino o una forma de reemplazo). 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La forma no se puede reemplazar o se pueden usar como una forma de reemplazo.  <br/> Para una forma en el lienzo, se deshabilita el botón **Cambiar forma** cuando se selecciona la forma.  <br/> Para una forma en una galería de símbolos, la forma no aparece como una forma de reemplazo cuando se hace clic en el botón **Cambiar forma** .  <br/> |
|FALSE  <br/> |La forma puede ser reemplazada o usar como una forma de reemplazo.  <br/> |
   
## <a name="remarks"></a>Notas

Para obtener una referencia a la celda **LockReplace** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockReplace  <br/> |
   
Para obtener una referencia a la celda **LockReplace** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockReplace** <br/> |
   

