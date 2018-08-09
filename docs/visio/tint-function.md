---
title: TINT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifica el color aumentando su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro int.
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823419"
---
# <a name="tint-function"></a>Función TINT

Modifica el color aumentando su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro _int_ . 
  
## <a name="syntax"></a>Sintaxis

TINT (** *color* **, ** *int* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se aumenta la luminosidad del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

Los límites superiores e inferiores de luminosidad son 0 y 240, respectivamente. No hay ningún límite en el tamaño del número entero que se puede pasar para el parámetro _int_ , pero la luminosidad nunca supera estos límites. 
  

