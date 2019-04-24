---
title: DISTTOPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332693"
---
# <a name="disttopath-function"></a>Función DISTTOPATH

Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

DISTTOPATH (* * *sección* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatorio  <br/> |**Double** <br/> |Coordenada _x_del punto.  <br/> |
| _y_ <br/> |Obligatorio  <br/> |**Double** <br/> |Coordenada _y_del punto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Doble**
  
## <a name="remarks"></a>Comentarios

Microsoft Visio devuelve #REF! Si no existe la _sección_ . 
  
El valor devuelto es positivo si el punto se encuentra a la izquierda de la dirección del recorrido y negativo si se encuentra a la derecha.
  

