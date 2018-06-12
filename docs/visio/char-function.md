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
description: Devuelve el carácter ANSI para un número.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821741"
---
# <a name="char-function"></a>CHAR (función)

Devuelve el carácter ANSI para un número.
  
## <a name="syntax"></a>Sintaxis

CHAR (** *número* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Número** <br/> |El número cuyo carácter ANSI desea obtener.  <br/> |
   
## <a name="remarks"></a>Notas

La cadena resultante tiene un carácter de longitud. El parámetro de _número_ debe ser un entero entre 1 y 255 (ambos inclusive), o la función devuelve un error. 
  
## <a name="example"></a>Ejemplo

CHAR(9) 
  
Devuelve el carácter de tabulador. 
  

