---
title: FLOOR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Redondear un número hacia 0 (cero), al número entero siguiente o a la siguiente instancia de varios.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439901"
---
# <a name="floor-function"></a>Función FLOOR

Redondear un número hacia 0 (cero), al número entero siguiente o a la siguiente instancia de  _varios_.
  
## <a name="syntax"></a>Sintaxis

FLOOR(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número que desea redondear.  <br/> |
| _multiple_ <br/> |Obligatorio  <br/> |**Number** <br/> |El múltiple por el que redondear.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Si  _no_ se especifica multiple, el número se redondea hacia 0 al número entero siguiente. 
  
 _Número_ y  _múltiplo_ deben tener los mismos signos, o un #NUM! error se devuelve. Si no  _se_  _puede_ convertir un número o varios en un valor, #VALUE! error se devuelve. Si número  _o_  _múltiplo_ es 0, el resultado es 0. 
  
## <a name="example-1"></a>Ejemplo 1

FLOOR(3.7)
  
Devuelve 3.
  
## <a name="example-2"></a>Ejemplo 2

FLOOR(-3.7)
  
Devuelve -3.
  
## <a name="example-3"></a>Ejemplo 3

FLOOR(3.7, 0.5)
  
Devuelve 3,5.
  

