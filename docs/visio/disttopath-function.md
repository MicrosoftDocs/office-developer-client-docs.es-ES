---
title: DISTTOPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822009"
---
# <a name="disttopath-function"></a>Función DISTTOPATH

Devuelve la distancia más corta desde el punto representado por las coordenadas especificadas a un punto en la ruta de acceso.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

DISTTOPATH (** *sección* **, ** *x* **, ** *y* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _x_ <br/> |Obligatorio  <br/> |**Double** <br/> |La _x_-coordenadas del punto.  <br/> |
| _y_ <br/> |Obligatorio  <br/> |**Double** <br/> |La _y_-coordenadas del punto.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Double**
  
## <a name="remarks"></a>Comentarios

¡Microsoft Visio devuelve #REF! Si no existe la _sección_ . 
  
El valor devuelto es positivo si el punto se encuentra a la izquierda de la dirección del recorrido y negativo si se encuentra a la derecha.
  

