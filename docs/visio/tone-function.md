---
title: TONE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifica el color disminuyendo su saturación en la cantidad especificada en el parámetro int.
ms.openlocfilehash: be89764c849299288963c272f8ffb2d5d728f270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823429"
---
# <a name="tone-function"></a>TONE (función)

Modifica el color disminuyendo su saturación en la cantidad especificada en el parámetro _int_ . 
  
## <a name="syntax"></a>Sintaxis

TONO (** *color* **, ** *int* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se reduce la saturación del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Notas

Los límites superiores e inferiores de saturación son 0 y 240, respectivamente. No hay ningún límite en el tamaño del número entero que se puede pasar para el parámetro _int_ , pero la saturación nunca supera estos límites. 
  

