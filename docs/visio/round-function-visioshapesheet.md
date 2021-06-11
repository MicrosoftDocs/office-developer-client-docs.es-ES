---
title: Función ROUND (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Redondear un número a la precisión representada por numberofdigits .
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439971"
---
# <a name="round-function-visioshapesheet"></a>Función ROUND (VisioShapeSheet)

Redondear un número a la precisión representada por  *numberofdigits*  . 
  
## <a name="syntax"></a>Sintaxis

ROUND(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número que desea redondear.  <br/> |
| _numberofdigits_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número de posiciones decimales de precisión.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si  _numberofdigits_ es mayor que 0,  _el_ número se redondea  _por numberofdigits_ a la derecha del decimal. Si  _numberofdigits_ es 0,  _el número_ se redondea a un número entero. Si  _numberofdigits_ es menor que 0,  _el_ número se redondea  _por numberofdigits_ a la izquierda del decimal. 
  
## <a name="example-1"></a>Ejemplo 1

ROUND(123.654,2)
  
Devuelve 123,65.
  
## <a name="example-2"></a>Ejemplo 2

ROUND(123.654,0)
  
Devuelve 124.
  
## <a name="example-3"></a>Ejemplo 3

ROUND(123.654,-1)
  
Devuelve 120.
  

