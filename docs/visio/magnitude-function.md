---
title: MAGNITUDE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Devuelve la magnitud del vector cuyo aumento es A y cuya ejecución es B, multiplicado por las respectivas constantes constante y constante.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317818"
---
# <a name="magnitude-function"></a>Función MAGNITUDE

Devuelve la magnitud del vector cuyo aumento es _a_ y cuya ejecución es _B_, multiplicado por las respectivas constantes _constante_ y _constante_. 
  
## <a name="syntax"></a>Sintaxis

MAGNITUDe (* * *constante* * *, * * *A* * *, * * *constante* * *, * * *B* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Constante_ <br/> |Obligatorio  <br/> |**Number** <br/> |La constante por la que multiplicar el aumento.  <br/> |
| _A_ <br/> |Obligatorio  <br/> |**Number** <br/> |El aumento.  <br/> |
| _Constante_ <br/> |Obligatorio  <br/> |**Number** <br/> |La constante por la que multiplicar la ejecución.  <br/> |
| _B_ <br/> |Obligatorio  <br/> |**Number** <br/> |La ejecución.  <br/> |
   
## <a name="remarks"></a>Comentarios

La MAGNITUD se calcula de acuerdo con la siguiente fórmula:
  
SQRT ((constante \* A) ^ 2 + (constante \* B) ^ 2)
  
## <a name="example"></a>Ejemplo

MAGNITUDE(1; 3; 1; 4) 
  
Devuelve 5. 
  

