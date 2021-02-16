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
description: Devuelve una polilínea. Esta función se usa en la celda A de las filas de geometría PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426299"
---
# <a name="polyline-function"></a>Función POLYLINE

Devuelve una polilínea. Esta función se usa en la celda A de las filas de geometría PolyLineTo. 
  
## <a name="syntax"></a>Sintaxis

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica cómo interpretar los datos _de entrada x._ Si  _xType_ es 0, la  _entrada x_-data se interpreta como un porcentaje de Width. Si  _xType_ es 1, la  _entrada x_-data se interpreta como una coordenada local.  <br/> |
| _yType_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica cómo interpretar los datos _de y-input._ Si  _yType_ es 0, la  _entrada y_-data se interpreta como un porcentaje de Height. Si  _yType_ es 1, la  _entrada y_-data se interpreta como una coordenada local.  <br/> |
| _x1_ <br/> |Obligatorio  <br/> |**Number** <br/> | _Coordenada x._  <br/> |
| _y1_ <br/> |Obligatorio  <br/> |**Number** <br/> |_Coordenada y._  <br/> |
   
## <a name="remarks"></a>Comentarios

Para cada  *argumento x,*  debe haber un  *argumento y;*  de lo contrario, se devuelve un error. 
  
## <a name="example"></a>Ejemplo

POLYLINE ( 0; 0; 0; 0; 0; 1; 1; 1; 1; 0; 0; 0) 
  
Devuelve un rectángulo de dimensiones Ancho x Alto. 
  

