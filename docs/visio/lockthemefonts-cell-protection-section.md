---
title: Celda LockThemeFonts (sección protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impide que se modifique la celda FontIndex de la fila propiedades del tema mediante la aplicación de un tema nuevo. No impide que los usuarios editen manualmente este valor en la ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421231"
---
# <a name="lockthemefonts-cell-protection-section"></a>Celda LockThemeFonts (sección protección)

Impide que se modifique la celda **FontIndex** de la fila **propiedades del tema** mediante la aplicación de un tema nuevo. No impide que los usuarios editen manualmente este valor en la ShapeSheet. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |No se puede cambiar el valor actual de la celda **FontIndex** a no ser que se cambie directamente en la ShapeSheet.  <br/> |
|FALSE  <br/> |La celda **FontIndex** puede cambiarse de su valor actual cuando se cambia el tema.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockThemeFonts** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockThemeFonts  <br/> |
   
Para obtener una referencia desde un programa a la celda **LockThemeFonts** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockThemeFonts** <br/> |
   

