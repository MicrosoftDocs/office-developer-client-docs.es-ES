---
title: SEGMENTCOUNT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Devuelve el número de segmentos de línea que conforma la ruta de acceso.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823130"
---
# <a name="segmentcount-function"></a>Función SEGMENTCOUNT

Devuelve el número de segmentos de línea que conforma la ruta de acceso.
  
## <a name="syntax"></a>Sintaxis

SEGMENTCOUNT (** *pathRef* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  
## <a name="remarks"></a>Observaciones

Los saltos de línea no se incluyen en el número total de segmentos devuelto.
  

