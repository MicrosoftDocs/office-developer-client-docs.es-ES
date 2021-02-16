---
title: Celda LockThemeIndex (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impide que la celda ThemeIndex de la fila Propiedades del tema se altere aplicando un tema nuevo o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411242"
---
# <a name="lockthemeindex-cell-protection-section"></a>Celda LockThemeIndex (Sección de protección)

Impide **que la celda ThemeIndex** de la fila **Propiedades** del tema se altere aplicando un tema nuevo o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en ShapeSheet. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |La **celda ThemeIndex** no se puede cambiar desde su valor actual a menos que se cambie directamente en la ShapeSheet.  <br/> |
|FALSE  <br/> |La **celda ThemeIndex** se puede cambiar desde su valor actual cuando se cambia el tema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockThemeIndex** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** o desde un programa mediante la propiedad **CellsU,** utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockThemeIndex  <br/> |
   
Para obtener una referencia desde un programa a la celda **LockThemeIndex** por su índice, utilice la **propiedad CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockThemeIndex** <br/> |
   

