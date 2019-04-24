---
title: AND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Devuelve TRUE (1) si todas las expresiones lógicas proporcionadas son TRUE. Si alguna de las expresiones lógicas es FALSE o 0, la función AND devuelve FALSE (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341562"
---
# <a name="and-function"></a>Función AND

Devuelve TRUE (1) si todas las expresiones lógicas proporcionadas son TRUE. Si alguna de las expresiones lógicas es FALSE o 0, la función AND devuelve FALSE (0).
  
## <a name="syntax"></a>Sintaxis

AND (* * *logical expresión1* * *, * * *logical expression2* * *,..., * * *logical expresión* in * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expresión lógica_ <br/> |Obligatorio  <br/> |**String** <br/> | Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor. Cualquier expresión que al evaluarse se convierta en un valor distinto de cero se considera verdadera.  <br/> |
   
## <a name="example"></a>Ejemplo

AND (altura \> 1, PinX \> 1)
  
Devuelve TRUE si ambas expresiones son verdaderas. Devuelve FALSE si cualquiera de las expresiones es falsa.
  

