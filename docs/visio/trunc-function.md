---
title: TRUNC (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Devuelve un número truncado al número de dígitos especificado.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426502"
---
# <a name="trunc-function"></a>Función TRUNC

Devuelve un número truncado al número de dígitos especificado.
  
## <a name="syntax"></a>Sintaxis

TRUNC(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El número que desea truncar.  <br/> |
| _numberofdigits_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |Número de dígitos a los que se va a truncar _el número._  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numérico.
  
## <a name="remarks"></a>Comentarios

Si  _numberofdigits_ es mayor que 0,  _el_ número se trunca a  _numberofdigits_ a la derecha del decimal. Si  _numberofdigits_ es 0,  _el número_ se trunca en un entero. Si  _numberofdigits_ es menor que 0,  _el_ número se trunca a  _numberofdigits_ a la izquierda del decimal. 
  
## <a name="example-1"></a>Ejemplo 1

TRUNC(123.654,2)
  
Devuelve 123,65.
  
## <a name="example-2"></a>Ejemplo 2

TRUNC(123.654,0)
  
Devuelve 123.
  
## <a name="example-3"></a>Ejemplo 3

TRUNC(123.654,-1)
  
Devuelve 120.
  

