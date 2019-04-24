---
title: SEGMENTCOUNT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Devuelve el número de segmentos de línea que conforma la ruta de acceso.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326043"
---
# <a name="segmentcount-function"></a>Función SEGMENTCOUNT

Devuelve el número de segmentos de línea que conforma la ruta de acceso.
  
## <a name="syntax"></a>Sintaxis

SEGMENTCOUNT (* * *pathRef* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Comentarios

Los saltos de línea no se incluyen en el número total de segmentos devuelto.
  

