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
description: Devuelve la magnitud del vector cuyo aumento es A y cuyo run es B, multiplicado por las constantes respectivas constantA y constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420461"
---
# <a name="magnitude-function"></a>Función MAGNITUDE

Devuelve la magnitud del vector cuyo aumento es  _A_ y cuya ejecución es  _B_, multiplicada por las constantes respectivas  _constantA_ y  _constantB_. 
  
## <a name="syntax"></a>Sintaxis

MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Obligatorio  <br/> |**Number** <br/> |La constante por la que multiplicar el aumento.  <br/> |
| _A_ <br/> |Obligatorio  <br/> |**Number** <br/> |El aumento.  <br/> |
| _constantB_ <br/> |Obligatorio  <br/> |**Number** <br/> |La constante por la que multiplicar la ejecución.  <br/> |
| _B_ <br/> |Obligatorio  <br/> |**Number** <br/> |La ejecución.  <br/> |
   
## <a name="remarks"></a>Comentarios

La MAGNITUD se calcula de acuerdo con la siguiente fórmula:
  
SQRT((constantA \* A)^2 + (constantB \* B)^2)
  
## <a name="example"></a>Ejemplo

MAGNITUDE(1; 3; 1; 4) 
  
Devuelve 5. 
  

