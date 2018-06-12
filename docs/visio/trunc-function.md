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
description: Devuelve un número truncado al número de decimales especificado.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823442"
---
# <a name="trunc-function"></a>TRUNC (función)

Devuelve un número truncado al número de decimales especificado.
  
## <a name="syntax"></a>Sintaxis

TRUNC (** *número* **, ** *númeroDeDígitos* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El número que desea truncar.  <br/> |
| _igual_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El número de dígitos al que se trunque _número_.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numeric.
  
## <a name="remarks"></a>Observaciones

Si _es mayor que 0,_ _número_ se trunca a _númeroDeDígitos_ a la derecha del separador decimal. Si es _igual_ a 0, _número_ se trunca a un valor entero. Si _es menor que 0,_ _número_ se trunca a _númeroDeDígitos_ a la izquierda del separador decimal. 
  
## <a name="example-1"></a>Ejemplo 1

TRUNC(123.654,2)
  
Devuelve 123,65.
  
## <a name="example-2"></a>Ejemplo 2

TRUNC(123.654,0)
  
Devuelve 123.
  
## <a name="example-3"></a>Ejemplo 3

TRUNC(123.654,-1)
  
Devuelve 120.
  

