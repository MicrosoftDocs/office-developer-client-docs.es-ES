---
title: SHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica el color disminuyendo su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382984"
---
# <a name="shade-function"></a>Función SHADE

Modifica el color disminuyendo su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro _int_ . 
  
## <a name="syntax"></a>Sintaxis

TONO (** *color* **, ** *int* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se disminuye la luminosidad del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Comentarios

Los límites superiores e inferiores de luminosidad son 0 y 240, respectivamente. No hay ningún límite en el tamaño del número entero que se puede pasar para el parámetro _int_ , pero la luminosidad nunca supera estos límites. 
  
![Límites superior e inferior de luminosidad](media/image199_ZA10173627.gif)
  

