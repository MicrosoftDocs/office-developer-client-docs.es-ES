---
title: Celda LockThemeConnectors (sección Protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Impide que la celda ConnectorsSchemeIndex en la fila de propiedades del tema que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet.
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822532"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Celda LockThemeConnectors (sección Protección)

Impide que la celda **ConnectorsSchemeIndex** en la fila de **Propiedades del tema** que se modifiquen aplicar un tema nuevo o seleccionando una nueva combinación de conector. Impedir que los usuarios editen manualmente este valor en la hoja ShapeSheet. 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|TRUE  <br/> |No se puede cambiar la celda **ConnectorsSchemeIndex** desde su valor actual a menos que cambie directamente en la hoja ShapeSheet.  <br/> |
|FALSE  <br/> |Puede cambiar la celda **ConnectorsSchemeIndex** desde su valor actual a través de la interfaz de usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para obtener una referencia a la celda **LockThemeConnectors** por su nombre desde otra fórmula, por el valor del atributo **N** de un elemento de **celda** , o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
| Nombre de celda:  <br/> | LockThemeConnectors  <br/> |
   
Para obtener una referencia a la celda **LockThemeConnectors** por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
| Índice de sección:  <br/> |**visSectionObject** <br/> |
| Índice de fila:  <br/> |**visRowLock** <br/> |
| Índice de celda:  <br/> |**visLockThemeConnectors** <br/> |
   

