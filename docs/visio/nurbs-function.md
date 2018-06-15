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
description: Devuelve una B-spline racional no uniforme (NURBS). Esta función se usa en la celda E de las filas de geometría NURBSTo.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19822719"
---
# <a name="nurbs-function"></a>NURBS (función)

Devuelve una B-spline racional no uniforme (NURBS). Esta función se usa en la celda E de las filas de geometría NURBSTo.
  
## <a name="syntax"></a>Sintaxis

NURBS (** *últimoPunto* **, ** *grado* **, ** *tipoDeX* **, ** *tipoDeY* **, ** *x1* **, ** *y1* **, ** *punto1* **, ** *grosor1* **, …) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _últimoPunto_ <br/> |Obligatorio  <br/> |**string** <br/> | El último nodo.  <br/> |
| _grado_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El grado de la spline.  <br/> |
| _tipoDeX_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Especifica cómo interpretar los datos de entrada de _x_ . Si el _valor de tipoDeX_ es 0, todos los datos de entrada de _x_ se interpreta como un porcentaje del ancho. Si _es 1,_ todos los datos de entrada de _x_ se interpreta como coordenadas locales.  <br/> |
| _dos valores_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Especifica cómo interpretar los datos de entrada de _y_ . Si _es 0,_ todos los datos de entrada _y_ se interpreta como un porcentaje del alto. Si _es 1,_ todos los datos de entrada de _y_ se interpretan como coordenadas locales.  <br/> |
| _X1_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada x.  <br/> |
| _Y1_ <br/> |Obligatorio  <br/> |**String** <br/> |Una coordenada y.  <br/> |
| _punto1_ <br/> |Obligatorio  <br/> |**String** <br/> |Un nodo de la spline B.  <br/> |
| _grosor1_ <br/> |Obligatorio  <br/> |**String** <br/> |Un grosor de la spline B.  <br/> |
   
## <a name="remarks"></a>Observaciones

Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error. 
  
Debe especificar al menos una *x*, *y*, *nodo* y argumento de *peso* ; de lo contrario, Visio devuelve un error. 
  

