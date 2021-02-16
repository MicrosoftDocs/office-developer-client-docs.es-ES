---
title: Celda LockFromGroupFormat (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426061"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>Celda LockFromGroupFormat (Sección de protección)

Impide que los cambios de formato de una forma de grupo se propaguen a sus subformas, a la vez que permite a los usuarios dar formato directamente a las subformas seleccionadas. 
  
El valor de la celda LockFromGroupFormat corresponde a configuración de la casilla de verificación **Contra formato en grupo** del cuadro de diálogo **Protección**. 
  
Para hacer referencia a la celda LockFromGroupFormat por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:

 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockFromGroupFormat  <br/> |
   
Para hacer referencia desde un programa a la celda LockFromGroupFormat según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes: 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockFromGroupFormat** <br/> |
   
El valor predeterminado de la celda es 0 (False).
  

