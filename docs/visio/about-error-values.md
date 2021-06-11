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
ms.openlocfilehash: 5219becdd1af888e424a2fe33faa7df5a06f61fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423870"
---
# <a name="about-error-values"></a>Valores de error

Los valores de error se muestran en las celdas que contienen fórmulas incorrectas.
  
Si una fórmula hace referencia a una celda que contiene un valor de error, también mostrará un valor de error. Puede utilizar las funciones ISERR, ISERRNA, ISERROR o ISERRVALUE para buscar valores de error.
  
**Valores de error**

||||
|:-----|:-----|:-----|
|**Si en la celda aparece** <br/> |**La fórmula contiene** <br/> |**Ejemplo** <br/> |
| #DIV/0!  <br/> |División entre cero  <br/> |10/0  <br/> |
| #VALUE!  <br/> | Argumento u operando de tipo no válido  <br/> | 5 + "Casa"  <br/> |
| #REF!  <br/> | Referencia a una celda que no existe  <br/> | Una celda hace referencia a otra que ya no existe  <br/> |
| #NUM!  <br/> | Número no válido  <br/> | Raíz cuadrada de un número negativo  <br/> |
| #N/A!  <br/> | No es un valor disponible  <br/> | Función NA( )  <br/> |
| #DIM!  <br/> | Valor dimensional que supera el intervalo de dimensiones (los poderes válidos son enteros -128 \< = n \< = 127)  <br/> Valor dimensional utilizado en una operación no válida  <br/> |1in^100 \* 1in^100 (el resultado es 1in^200, que está más allá del intervalo de dimensiones)  <br/> 5,2cm^1,5 (exponente no entero)  <br/> |
   

