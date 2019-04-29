---
title: Celda LockThemeConnectors (sección protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impide que se modifique la celda ConnectorsSchemeIndex de la fila propiedades del tema aplicando un nuevo tema o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en la ShapeSheet.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438410"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Celda LockThemeConnectors (sección protección)

Impide que se modifique la celda **ConnectorsSchemeIndex** de la fila **propiedades del tema** aplicando un nuevo tema o seleccionando un nuevo esquema de conector. No impide que los usuarios editen manualmente este valor en la ShapeSheet. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |No se puede cambiar el valor actual de la celda **ConnectorsSchemeIndex** a no ser que se cambie directamente en la ShapeSheet.  <br/> |
|FALSE  <br/> |La celda **ConnectorsSchemeIndex** se puede cambiar de su valor actual a través de la interfaz de usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockThemeConnectors** por su nombre desde otra fórmula, por valor del atributo **N** de un elemento **Cell** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockThemeConnectors  <br/> |
   
Para obtener una referencia desde un programa a la celda **LockThemeConnectors** por su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockThemeConnectors** <br/> |
   

