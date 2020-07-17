---
title: ANGLEALONGPATH (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160296"
---
# <a name="anglealongpath-function"></a>Función ANGLEALONGPATH

Devuelve el ángulo de la tangente a la ruta de acceso en un punto dado.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

ANGLEALONGPATH (***sección***, ***viaje*** ***[, segmento]*** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obligatorio  <br/> |**String** <br/> |Sección de geometría que representa la ruta de acceso, especificada por una referencia a su celda Path (por ejemplo, Geometry1.Path).  <br/> |
| _carrera_ <br/> |Obligatorio  <br/> |**Double** <br/> |Porcentaje a lo largo de la ruta de acceso, desde el punto inicial hasta el punto final. Debe ser un valor entre 0 y 1.  <br/> |
| _segmentos_ <br/> |Opcional  <br/> |**Integer** <br/> |Segmento basado en 1 de la ruta de acceso en el cual se calcula el ángulo de la tangente.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

 **Doble**
  
## <a name="remarks"></a>Comentarios

Si incluye un valor de _segmento_ , ANGLEALONGPATH devuelve el valor solo para ese segmento. 
  
Si incluye un valor de _segmento_ , ANGLEALONGPATH determina el punto de la tangente mediante _viajar_ para calcular el percert a lo largo del _segmento_.
  
Si no existe ninguna _sección_ o _segmento_ , Microsoft Visio devuelve #REF!. 
  

