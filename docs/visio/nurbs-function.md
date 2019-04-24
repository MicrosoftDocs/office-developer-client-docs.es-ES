---
title: NURBS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Devuelve una spline B racional no uniforme (NURBS). Esta función se utiliza en la celda E de las filas de geometría NURBSto.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340127"
---
# <a name="nurbs-function"></a>Función NURBS

Devuelve una spline B racional no uniforme (NURBS). Esta función se utiliza en la celda E de las filas de geometría NURBSto.
  
## <a name="syntax"></a>Sintaxis

NURBS (* * *knotLast* * *, * * *degree* * *, * * *tipoDex* * *, * * *tipoDeY* * *, * * *x1* * *, * * *Y1* * *, * * *knot1* * *, * * *Weight1* * *,...) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Obligatorio  <br/> |**string** <br/> | El último nodo.  <br/> |
| _grado_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El grado de la spline.  <br/> |
| _Alguno_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Especifica cómo interpretar los datos de entrada _x_ . Si _tipoDex_ es 0, todos los datos de entrada _x_ se interpretan como un porcentaje del ancho. Si _tipoDex_ es 1, todos los datos de entrada _x_ se interpretan como coordenadas locales.  <br/> |
| _tipoDeY_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Especifica cómo interpretar los datos de entrada de _y_ . Si el valor de _tipoDeY_ es 0, todos los datos de entrada de _y_ se interpretan como un porcentaje del alto. Si _tipoDeY_ es 1, todos los datos de entrada de _y_ se interpretan como coordenadas locales.  <br/> |
| _1_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada x.  <br/> |
| _a1_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada y.  <br/> |
| _knot1_ <br/> |Obligatorio  <br/> |**String** <br/> |Un nodo de la spline B.  <br/> |
| _Weight1_ <br/> |Obligatorio  <br/> |**String** <br/> |Un grosor de la spline B.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error. 
  
Debe especificar al menos un argumento *x*, *y*, *nudo* y *Weight* ; de lo contrario, Visio devuelve un error. 
  

