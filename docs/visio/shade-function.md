---
title: SHADE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifica el color disminuyendo su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro int.
ms.openlocfilehash: 4a02aa41050c3cf36b567c238670b5f61074bd7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823133"
---
# <a name="shade-function"></a>SHADE (función)

Modifica el color disminuyendo su luminosidad según la cantidad (positiva o negativa) especificado en el parámetro _int_ . 
  
## <a name="syntax"></a>Sintaxis

TONO (** *color* **, ** *int* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Índice de color de Microsoft Visio o valor RGB del color.  <br/> |
| _int_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Cantidad por la que se disminuye la luminosidad del color. Puede ser positiva o negativa.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **RVA**
  
## <a name="remarks"></a>Notas

Los límites superiores e inferiores de luminosidad son 0 y 240, respectivamente. No hay ningún límite en el tamaño del número entero que se puede pasar para el parámetro _int_ , pero la luminosidad nunca supera estos límites. 
  
![](media/image199_ZA10173627.gif)
  

