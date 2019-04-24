---
title: TINT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifica el color aumentando su luminosidad por la cantidad (positiva o negativa) especificada en el parámetro int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280934"
---
# <a name="tint-function"></a>Función TINT

Modifica el color aumentando su luminosidad por la cantidad (positiva o negativa) especificada en el parámetro _int_ . 
  
## <a name="syntax"></a>Sintaxis

MATIZ (* * *color* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se aumenta la luminosidad del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

Los límites superior o inferior de luminosidad son 0 y 240, respectivamente. No hay ningún límite en el tamaño del número entero que puede pasar para el parámetro _int_ , pero la luminosidad nunca supera estos límites. 
  

