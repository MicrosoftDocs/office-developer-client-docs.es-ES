---
title: Celda LockFromGroupFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822522"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>Celda LockFromGroupFormat (Sección de protección)

Bloques de cambios de formato a una forma de grupo de que se propaga a sus subformas, mientras permite a los usuarios dar formato a las subformas seleccionadas directamente. 
  
El valor de la celda LockFromGroupFormat corresponde a la opción de casilla de verificación **contra formato en grupo** en el cuadro de diálogo **protección** . 
  
Para hacer referencia a la celda LockFromGroupFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU** , utilice: 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockFromGroupFormat  <br/> |
   
Para hacer referencia a la celda LockFromGroupFormat por su índice desde un programa, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockFromGroupFormat** <br/> |
   
El valor predeterminado de la celda es 0 (False).
  

