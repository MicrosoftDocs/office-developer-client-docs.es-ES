---
title: POLYLINE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Devuelve una polilínea. Esta función se usa en la celda a de las filas de geometría PolyLineTo.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822766"
---
# <a name="polyline-function"></a>POLYLINE (función)

Devuelve una polilínea. Esta función se usa en la celda a de las filas de geometría PolyLineTo. 
  
## <a name="syntax"></a>Sintaxis

POLYLINE (** *tipoDeX* **, ** *tipoDeY* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _tipoDeX_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica cómo interpretar los datos de entrada de _x_ . _Si es 0, la entrada _x__ -datos x se interpretan como un porcentaje del ancho. _Si es 1, la entrada _x__ -datos se interpretan como una coordenada local.  <br/> |
| _dos valores_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica cómo se debe interpretar la _y_-datos de entrada. _Si es 0, la entrada _y__ -datos de x se interpretan como un porcentaje del alto. _Si es 1, la entrada _y__ -datos se interpretan como una coordenada local.  <br/> |
| _X1_ <br/> |Obligatorio  <br/> |**Número** <br/> | Una _x_-coordinar.  <br/> |
| _Y1_ <br/> |Obligatorio  <br/> |**Número** <br/> |Un _y_-coordinar.  <br/> |
   
## <a name="remarks"></a>Notas

Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error. 
  
## <a name="example"></a>Ejemplo

POLYLINE ( 0; 0; 0; 0; 0; 1; 1; 1; 1; 0; 0; 0) 
  
Devuelve un rectángulo de dimensiones Ancho x Alto. 
  

