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
description: Evalúa una de las dos expresiones en función del valor de estado.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420349"
---
# <a name="userui-function"></a>Función USERUI

Evalúa una de las dos expresiones según el valor de  _estado_.
  
## <a name="syntax"></a>Sintaxis

USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Determina qué expresión evaluar.  <br/> |
| _defaultexpression_ <br/> |Obligatorio  <br/> |**String** <br/> |Expresión predeterminada.  <br/> |
| _userexpression_ <br/> |Obligatorio  <br/> |**String** <br/> |Expresión proporcionada por el usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si  _el_ estado es 0, la función USERUI evalúa la  _expresión predeterminada_. Si _el_ estado es 1, evalúa la _expresión user ._
  
## <a name="example"></a>Ejemplo

USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75) 
  
Evalúa la expresión Width \* .075 y devuelve el resultado. 
  

