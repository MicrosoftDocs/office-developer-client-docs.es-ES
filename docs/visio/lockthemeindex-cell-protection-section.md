---
title: Celda LockThemeIndex (sección protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impide que se modifique la celda ThemeIndex de las propiedades del tema aplicando un nuevo tema o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en la ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358082"
---
# <a name="lockthemeindex-cell-protection-section"></a>Celda LockThemeIndex (sección protección)

Impide que se modifique la celda **ThemeIndex** de **las propiedades del tema** aplicando un nuevo tema o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en la ShapeSheet. 
  
|**Value**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |No se puede cambiar el valor actual de la celda **ThemeIndex** a no ser que se cambie directamente en la ShapeSheet.  <br/> |
|FALSE  <br/> |La celda **ThemeIndex** puede cambiarse de su valor actual cuando se cambia el tema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockThemeIndex** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockThemeIndex  <br/> |
   
Para obtener una referencia desde un programa a la celda **LockThemeIndex** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockThemeIndex** <br/> |
   

