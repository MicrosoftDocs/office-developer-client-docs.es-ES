---
title: PATHSEGMENT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Devuelve el número de segmento basado en 1 en la marca de porcentaje especificada a lo largo de la ruta de acceso especificada.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344453"
---
# <a name="pathsegment-function"></a>Función PATHSEGMENT

Devuelve el número de segmento basado en 1 en la marca de porcentaje especificada a lo largo de la ruta de acceso especificada.
  
## <a name="syntax"></a>Sintaxis

PATHSEGMENT (* * *sección* * *, * * *viaje* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _carrera_ <br/> |Obligatorio  <br/> |**Double** <br/> |Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final. Debe oscilar entre 0 y 1.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  

