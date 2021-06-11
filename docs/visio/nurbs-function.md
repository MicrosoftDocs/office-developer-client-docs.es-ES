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
description: Devuelve una spline B racional no uniforme (NURBS). Esta función se usa en la celda E de las filas de geometría NURBSTo.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438459"
---
# <a name="nurbs-function"></a>Función NURBS

Devuelve una spline B racional no uniforme (NURBS). Esta función se usa en la celda E de las filas de geometría NURBSTo.
  
## <a name="syntax"></a>Sintaxis

NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |Obligatorio  <br/> |**string** <br/> | El último nodo.  <br/> |
| _grado_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El grado de la spline.  <br/> |
| _xType_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Especifica cómo interpretar los datos _de entrada x._ Si  _xType_ es 0, todos  _los datos de entrada x_ se interpretan como un porcentaje de Width. Si  _xType_ es 1, todos los  _datos de entrada x_ se interpretan como coordenadas locales.  <br/> |
| _yType_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Especifica cómo interpretar los datos _de entrada y._ Si  _yType_ es 0, todos  _los datos de entrada y_ se interpretan como un porcentaje de Height. Si  _yType_ es 1, todos  _los datos de entrada y_ se interpretan como coordenadas locales.  <br/> |
| _x1_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada x.  <br/> |
| _y1_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada y.  <br/> |
| _knot1_ <br/> |Obligatorio  <br/> |**String** <br/> |Un nodo de la spline B.  <br/> |
| _weight1_ <br/> |Obligatorio  <br/> |**String** <br/> |Un grosor de la spline B.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para cada  *argumento x,*  debe haber un  *argumento y;*  de lo contrario, se devuelve un error. 
  
Debe especificar al menos un *argumento x*, *y*, *knot* y *weight;* de lo contrario, Visio devuelve un error. 
  

