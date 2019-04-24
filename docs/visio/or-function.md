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
description: Devuelve TRUE (1) si alguna de las expresiones lógicas pasadas como parámetros son TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337215"
---
# <a name="or-function"></a>Función OR

Devuelve TRUE (1) si alguna de las expresiones lógicas pasadas como parámetros son TRUE.
  
## <a name="syntax"></a>Sintaxis

OR (* * *logicalexpression1* * *, * * *logicalexpression2* * *,..., * * *logicalexpressionN* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera expresión cuya verdad desea evaluar.  <br/> |
| _logicalexpression2_ <br/> |Obligatorio  <br/> |**String** <br/> |La segunda expresión cuya verdad desea evaluar.  <br/> |
| _logicalexpressionN_ <br/> |Obligatorio  <br/> |**String** <br/> |La expresión n cuya verdad desea evaluar.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Comentarios

Cualquier expresión que dé como resultado un valor distinto de cero se considera verdadera. Si todas las expresiones lógicas son falsas o iguales a 0, esta función devuelve el valor FALSE. 
  
## <a name="example"></a>Ejemplo

O (altura \> 1, PinX \> 1) 
  
Devuelve TRUE (1) si cualquiera de las expresiones es verdadera. Devuelve FALSE (0) sólo cuando ambas expresiones son falsas. 
  

