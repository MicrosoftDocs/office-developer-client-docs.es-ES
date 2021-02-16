---
title: TONE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica el color disminuyendo su saturación por la cantidad especificada en el parámetro int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434378"
---
# <a name="tone-function"></a>Función TONE

Modifica el color disminuyendo su saturación por la cantidad especificada en el _parámetro int._ 
  
## <a name="syntax"></a>Sintaxis

TONE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se reduce la saturación del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

Los límites superior o inferior de saturación son 0 y 240, respectivamente. No hay ningún límite en el tamaño del entero que puedes pasar para el parámetro  _int,_ pero la saturación nunca supera estos límites. 
  

