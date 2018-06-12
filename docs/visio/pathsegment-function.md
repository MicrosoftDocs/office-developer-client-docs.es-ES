---
title: PATHSEGMENT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Devuelve el número de segmento basado en 1 en la marca de porcentaje especificado a lo largo de la ruta de acceso especificada.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822740"
---
# <a name="pathsegment-function"></a>PATHSEGMENT (función)

Devuelve el número de segmento basado en 1 en la marca de porcentaje especificado a lo largo de la ruta de acceso especificada.
  
## <a name="syntax"></a>Sintaxis

PATHSEGMENT (** *sección* **, ** *viajes* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _viajes_ <br/> |Obligatorio  <br/> |**Double** <br/> |Porcentaje de la ruta de acceso atravesado, desde el punto inicial al punto final. Debe oscilar entre 0 y 1.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Entero
  

