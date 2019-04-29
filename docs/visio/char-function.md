---
title: CHAR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Devuelve el carácter ANSI de un número.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418193"
---
# <a name="char-function"></a>Función CHAR

Devuelve el carácter ANSI de un número.
  
## <a name="syntax"></a>Sintaxis

CHAR (* * *Number* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número cuyo carácter ANSI desea obtener.  <br/> |
   
## <a name="remarks"></a>Comentarios

La cadena resultante tiene un carácter de longitud. El parámetro _número_ debe ser un entero entre 1 y 255 (inclusive), o la función devuelve un error. 
  
## <a name="example"></a>Ejemplo

CHAR (9) 
  
Devuelve el carácter de tabulador. 
  

