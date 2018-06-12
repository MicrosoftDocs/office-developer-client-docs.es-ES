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
description: Devuelve la magnitud del vector cuya elevación es A y cuya ejecución es B, multiplicada por sus respectivas constantes constante de a y constante.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822566"
---
# <a name="magnitude-function"></a>MAGNITUDE (función)

Devuelve la magnitud del vector cuya elevación es _A_ y cuya ejecución es _B_, multiplicada por sus respectivas constantes _constante_ de a y _constante_. 
  
## <a name="syntax"></a>Sintaxis

MAGNITUD (** *constante* **, ** *A* **, ** *constante* **, ** *B* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Constante_ <br/> |Obligatorio  <br/> |**Número** <br/> |La constante por la que multiplicar el aumento.  <br/> |
| _A_ <br/> |Obligatorio  <br/> |**Número** <br/> |El aumento.  <br/> |
| _constante de b_ <br/> |Obligatorio  <br/> |**Número** <br/> |La constante por la que multiplicar la ejecución.  <br/> |
| _B_ <br/> |Obligatorio  <br/> |**Número** <br/> |La ejecución.  <br/> |
   
## <a name="remarks"></a>Observaciones

La MAGNITUD se calcula de acuerdo con la siguiente fórmula:
  
SQRT ((constante \* A) ^ 2 + (constante de b \* B) ^ 2)
  
## <a name="example"></a>Ejemplo

MAGNITUDE(1; 3; 1; 4) 
  
Devuelve 5. 
  

