---
title: Valores de error
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251832
localization_priority: Normal
ms.assetid: 56430658-a798-c004-b4ba-363443f43ded
description: Los valores de error se muestran en las celdas que contienen fórmulas incorrectas.
ms.openlocfilehash: 301f566151362727daf8236f8ca88fca8758054e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821483"
---
# <a name="about-error-values"></a>Valores de error

Los valores de error se muestran en las celdas que contienen fórmulas incorrectas.
  
Si una fórmula hace referencia a una celda que contiene un valor de error, también mostrará un valor de error. Puede utilizar las funciones ISERR, ISERRNA, ISERROR o ISERRVALUE para buscar valores de error.
  
**Valores de error**

||||
|:-----|:-----|:-----|
|**Si la celda aparece** <br/> |**La fórmula contiene** <br/> |**Ejemplo** <br/> |
| #DIV/0!  <br/> |División por 0  <br/> |10/0  <br/> |
| #VALUE!  <br/> | Argumento u operando de tipo no válido  <br/> | 5 + "Corchos"  <br/> |
| #REF!  <br/> | Una referencia a una celda que no existe  <br/> | Una celda que hace referencia a otra celda que ya no existe  <br/> |
| #NUM!  <br/> | Un número no válido  <br/> | Raíz cuadrada de un número negativo  <br/> |
| #N/A!  <br/> | No es un valor disponible  <br/> | Función NA)  <br/> |
| ¡#DIM!  <br/> | Valor dimensional que excede el intervalo de la dimensión (exponentes válidos son enteros -128 \<= n \<= 127)  <br/> Un valor dimensional utilizado en una operación no válida  <br/> |1pda ^ 100 \* 1pda ^ 100 (el resultado es 1pda ^ 200, que está fuera del intervalo de dimensión)  <br/> 5.2 cm ^ 1,5 (exponente no entero)  <br/> |
   

