---
title: LOCALFORMULAEXISTS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Indica si la celda a la que se hace referencia contiene una fórmula local.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433293"
---
# <a name="localformulaexists-function"></a>Función LOCALFORMULAEXISTS

Indica si la celda a la que se hace referencia contiene una fórmula local. 
  
## <a name="syntax"></a>Sintaxis

LOCALFORMULAEXISTS (** *cellref* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Obligatorio  <br/> |**String** <br/> | La celda en la que se debe comprobar si existe una fórmula.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Comentarios

La función LOCALFORMULAEXISTS devuelve 1 si la celda contiene una fórmula local; si no es así o la fórmula es heredada, devuelve cero (0). 
  

