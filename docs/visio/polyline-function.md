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
description: Devuelve una polilínea. Esta función se usa en la celda A de las filas de geometría poliLíneas.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348282"
---
# <a name="polyline-function"></a>Función POLYLINE

Devuelve una polilínea. Esta función se usa en la celda A de las filas de geometría poliLíneas. 
  
## <a name="syntax"></a>Sintaxis

POLYLINE (* * *tipoDex* * *, * * *tipoDeY* * *, * * *x1* * *, * * *Y1* * *...) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _Alguno_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica cómo interpretar los datos de entrada _x_ . Si _tipoDex_ es 0, los datos de entrada _x_se interpretan como un porcentaje del ancho. Si _tipoDex_ es 1, los datos de entrada _x_se interpretan como una coordenada local.  <br/> |
| _tipoDeY_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica cómo interpretar los datos de entrada _y_. Si el valor de _tipoDeY_ es 0, los datos de entrada de _y_se interpretan como un porcentaje del alto. Si el de _tipoDeY_ es 1, los datos de entrada de _y_se interpretan como una coordenada local.  <br/> |
| _1_ <br/> |Obligatorio  <br/> |**Number** <br/> | Una coordenada _x_.  <br/> |
| _a1_ <br/> |Obligatorio  <br/> |**Number** <br/> |Una coordenada _y_.  <br/> |
   
## <a name="remarks"></a>Comentarios

Para cada argumento *x* debe haber un argumento *y* ; de lo contrario, se devuelve un error. 
  
## <a name="example"></a>Ejemplo

POLYLINE ( 0; 0; 0; 0; 0; 1; 1; 1; 1; 0; 0; 0) 
  
Devuelve un rectángulo de dimensiones Ancho x Alto. 
  

