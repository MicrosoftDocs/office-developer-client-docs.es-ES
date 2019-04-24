---
title: SHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica el color disminuyendo su luminosidad en función de la cantidad (positiva o negativa) especificada en el parámetro int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326603"
---
# <a name="shade-function"></a>Función SHADE

Modifica el color disminuyendo su luminosidad en función de la cantidad (positiva o negativa) especificada en el parámetro _int_ . 
  
## <a name="syntax"></a>Sintaxis

SHADE (* * *color* * *, * * *int* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se disminuye la luminosidad del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

Los límites superior o inferior de luminosidad son 0 y 240, respectivamente. No hay ningún límite en el tamaño del número entero que puede pasar para el parámetro _int_ , pero la luminosidad nunca supera estos límites. 
  
![Límites superior e inferior de la luminosidad](media/image199_ZA10173627.gif)
  

