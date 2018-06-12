---
title: USERUI (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Evalúa una de las dos expresiones dependiendo del valor de estado.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823500"
---
# <a name="userui-function"></a>USERUI (función)

Evalúa una de las dos expresiones dependiendo del valor de _estado_.
  
## <a name="syntax"></a>Sintaxis

USERUI (** *estado* **, ** *expresiónpredeterminada* **, ** *expresióndeusuario* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Determina qué expresión se evalúe.  <br/> |
| _expresiónpredeterminada_ <br/> |Obligatorio  <br/> |**String** <br/> |La expresión de forma predeterminada.  <br/> |
| _expresióndeusuario_ <br/> |Obligatorio  <br/> |**String** <br/> |Una expresión proporcionada por el usuario.  <br/> |
   
## <a name="remarks"></a>Notas

Si el _estado_ es 0, la función USERUI evalúa _expresiónpredeterminada_. Si _es 1,_ evalúa _expresióndeusuario_.
  
## <a name="example"></a>Ejemplo

USERUI (1, si (ancho\>6pda, 6pda, Width), Width\*0,75) 
  
Evalúa la expresión Width\*.075 y devuelve el resultado. 
  

