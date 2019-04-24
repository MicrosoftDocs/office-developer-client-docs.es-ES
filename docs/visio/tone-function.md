---
title: TONE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica el color disminuyendo su saturación en la cantidad especificada en el parámetro int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335689"
---
# <a name="tone-function"></a>Función TONE

Modifica el color disminuyendo su saturación en la cantidad especificada en el parámetro _int_ . 
  
## <a name="syntax"></a>Sintaxis

TONO (* * *color* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se reduce la saturación del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

Los límites superior o inferior de saturación son 0 y 240, respectivamente. No hay ningún límite en el tamaño del número entero que se puede pasar para el parámetro _int_ , pero la saturación nunca supera estos límites. 
  

