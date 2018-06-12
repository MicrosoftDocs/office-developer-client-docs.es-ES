---
title: ANGLEALONGPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821551"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH (función)

Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.
  
## <a name="version-information"></a>Información de versión

Versión agregada: Visio 2010 
  
## <a name="syntax"></a>Sintaxis

ANGLEALONGPATH (** *sección* **, ** *viajes* ** ** *[, segmento]* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _viajes_ <br/> |Obligatorio  <br/> |**Double** <br/> |Porcentaje a lo largo de la ruta de acceso, desde el punto inicial hasta el punto final. Debe ser un valor entre 0 y 1.  <br/> |
| _segmento_ <br/> |Opcional  <br/> |**Integer** <br/> |Segmento basado en 1 de la ruta de acceso en el cual se calcula el ángulo de la tangente.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Double**
  
## <a name="remarks"></a>Notas

Si incluye un valor _segment_ , ANGLEALONGPATH devuelve el valor solamente para ese segmento. 
  
Si incluye un valor _segment_ , ANGLEALONGPATH determina el punto de la tangente mediante el uso _de viajes_ para calcular la percertage a lo largo de _segmento_.
  
Si no existe _section_ ni _segment_ , Microsoft Visio devuelve #REF!. 
  

