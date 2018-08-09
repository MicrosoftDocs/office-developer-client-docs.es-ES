---
title: DEPENDSON (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Crea una dependencia de referencia de celda.
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821966"
---
# <a name="dependson-function"></a>Función DEPENDSON

Crea una dependencia de referencia de celda.
  
## <a name="syntax"></a>Sintaxis

DEPENDSON (** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _CellRef_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera referencia de celda.  <br/> |
| _cellref2_ <br/> |Opcional  <br/> |**String** <br/> |La segunda referencia de celda.  <br/> |
   
## <a name="remarks"></a>Observaciones

Esta función siempre devuelve el valor FALSE. No tiene ningún efecto cuando se utiliza en una celda Action o en una fila Event. 
  
## <a name="example"></a>Ejemplo

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Abre el bloque de texto de una forma siempre que cambien las celdas PinX o PinY de la forma. 
  

