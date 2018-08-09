---
title: Celda LockThemeFonts (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impide que la celda FontIndex en la fila de propiedades del tema que se modifica aplicando un tema nuevo. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822553"
---
# <a name="lockthemefonts-cell-protection-section"></a>Celda LockThemeFonts (sección Protección)

Impide que la celda **FontIndex** en la fila de **Propiedades del tema** que se modifica aplicando un tema nuevo. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |No se puede cambiar la celda **FontIndex** desde su valor actual a menos que cambie directamente en la hoja ShapeSheet.  <br/> |
|FALSE  <br/> |Puede cambiar el valor actual de la celda **FontIndex** cuando se cambia el tema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockThemeFonts** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockThemeFonts  <br/> |
   
Para obtener una referencia a la celda **LockThemeFonts** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockThemeFonts** <br/> |
   

