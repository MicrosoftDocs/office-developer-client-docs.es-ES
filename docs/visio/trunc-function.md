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
description: Devuelve un número truncado en el número de dígitos especificado.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335178"
---
# <a name="trunc-function"></a>Función TRUNC

Devuelve un número truncado en el número de dígitos especificado.
  
## <a name="syntax"></a>Sintaxis

TRUNC (* * *número* * *, * * *númeroDeDígitos* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |El número que desea truncar.  <br/> |
| _númeroDeDígitos_ <br/> |Obligatorio  <br/> |**Numeric** <br/> |Número de dígitos al que se va a truncar el _número_.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numérico.
  
## <a name="remarks"></a>Comentarios

Si _númeroDeDígitos_ es mayor que 0, el _número_ se trunca a _númeroDeDígitos_ a la derecha del separador decimal. Si _númeroDeDígitos_ es 0, el _número_ se trunca a un entero. Si _númeroDeDígitos_ es menor que 0, el _número_ se trunca _dejando númeroDeDígitos_ a la izquierda del separador decimal. 
  
## <a name="example-1"></a>Ejemplo 1

TRUNC (123.654, 2)
  
Devuelve 123,65.
  
## <a name="example-2"></a>Ejemplo 2

TRUNC (123.654, 0)
  
Devuelve 123.
  
## <a name="example-3"></a>Ejemplo 3

TRUNC (123.654,-1)
  
Devuelve 120.
  

