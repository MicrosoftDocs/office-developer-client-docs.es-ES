---
title: Celda LockThemeColors (Sección de protección)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 2ca8af2c7a41259af73a111af331ce1031e5f46c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822529"
---
# <a name="lockthemecolors-cell-protection-section"></a>Celda LockThemeColors (sección Protección)

Impide la aplicación de colores del tema a la forma. 
  
El valor de la celda LockThemeColors corresponde a configuración de la casilla de verificación **Contra colores del tema** del cuadro de diálogo **Protección**. 
  
Para hacer referencia a la celda LockThemeColors por su nombre desde otra fórmula, o desde un programa mediante la propiedad **CellsU**, utilice:

 
  
|||
|:-----|:-----|
|Nombre de celda:  <br/> |LockThemeColors  <br/> |
   
Para hacer referencia desde un programa a la celda LockThemeColors según su índice, utilice la propiedad **CellsSRC** con los argumentos siguientes:

 
  
|||
|:-----|:-----|
|Índice de sección:  <br/> |**visSectionObject** <br/> |
|Índice de fila:  <br/> |**visRowLock** <br/> |
|Índice de celda:  <br/> |**visLockThemeColors** <br/> |
   

