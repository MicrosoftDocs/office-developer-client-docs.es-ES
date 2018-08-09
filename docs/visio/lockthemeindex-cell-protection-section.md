---
title: Celda LockThemeIndex (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impide que ThemeIndex de celda en la fila de propiedades del tema que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822535"
---
# <a name="lockthemeindex-cell-protection-section"></a>Celda LockThemeIndex (sección Protección)

Impide que **ThemeIndex** de celda en la fila de **Propiedades del tema** que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |No se puede cambiar la celda **ThemeIndex** desde su valor actual a menos que cambie directamente en la hoja ShapeSheet.  <br/> |
|FALSE  <br/> |Puede cambiar el valor actual de la celda **ThemeIndex** cuando se cambia el tema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockThemeIndex** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockThemeIndex  <br/> |
   
Para obtener una referencia a la celda **LockThemeIndex** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockThemeIndex** <br/> |
   

