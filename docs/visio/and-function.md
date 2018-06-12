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
description: Devuelve TRUE (1) si todas las expresiones lógicas suministradas son TRUE. Si alguna de las expresiones lógicas es falso o 0, la función y devuelve FALSE (0).
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821540"
---
# <a name="and-function"></a>AND (función)

Devuelve TRUE (1) si todas las expresiones lógicas suministradas son TRUE. Si alguna de las expresiones lógicas es falso o 0, la función y devuelve FALSE (0).
  
## <a name="syntax"></a>Sintaxis

Y (** *expression1 lógica* **, ** *Expresión2 lógica* **,..., ** *expresiónn lógico* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expresión lógica_ <br/> |Obligatorio  <br/> |**String** <br/> | Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor. Cualquier expresión que al evaluarse se convierta en un valor distinto de cero se considera verdadera.  <br/> |
   
## <a name="example"></a>Ejemplo

Y (alto \> 1, PinX \> 1)
  
Devuelve TRUE si ambas expresiones son verdaderas. Devuelve FALSE si cualquiera de las expresiones es falsa.
  

