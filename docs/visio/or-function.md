---
title: OR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Devuelve TRUE (1) si cualquiera de las expresiones lógicas que se pasan como parámetros son TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822702"
---
# <a name="or-function"></a>Función OR

Devuelve TRUE (1) si cualquiera de las expresiones lógicas que se pasan como parámetros son TRUE.
  
## <a name="syntax"></a>Sintaxis

O (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera expresión cuya verdad desea evaluar.  <br/> |
| _logicalexpression2_ <br/> |Obligatorio  <br/> |**String** <br/> |La segunda expresión cuya verdad desea evaluar.  <br/> |
| _logicalexpressionN_ <br/> |Obligatorio  <br/> |**String** <br/> |La expresión n cuya verdad desea evaluar.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Observaciones

Cualquier expresión que dé como resultado un valor distinto de cero se considera verdadera. Si todas las expresiones lógicas son falsas o iguales a 0, esta función devuelve el valor FALSE. 
  
## <a name="example"></a>Ejemplo

O (alto \> 1, PinX \> 1) 
  
Devuelve TRUE (1) si cualquiera de las expresiones es verdadera. Devuelve FALSE (0) sólo cuando ambas expresiones son falsas. 
  

