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
description: Indica si la celda referida contiene una fórmula local.
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822499"
---
# <a name="localformulaexists-function"></a>Función LOCALFORMULAEXISTS

Indica si la celda referida contiene una fórmula local. 
  
## <a name="syntax"></a>Sintaxis

LOCALFORMULAEXISTS (** *cellref* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Obligatorio  <br/> |**String** <br/> | La celda en la que se debe comprobar si existe una fórmula.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Observaciones

La función LOCALFORMULAEXISTS devuelve 1 si la celda contiene una fórmula local; si no es así o la fórmula es heredada, devuelve cero (0). 
  

