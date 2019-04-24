---
title: POW (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Devuelve un número elevado a la potencia de un exponente.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356052"
---
# <a name="pow-function"></a>Función POW

Devuelve un número elevado a la potencia de un exponente.
  
## <a name="syntax"></a>Sintaxis

POW (* * *Number* * *, * * ** exponente * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número para elevar la potencia del exponente.  <br/> |
| _exponent_ <br/> |Obligatorio  <br/> |**Number** <br/> |El exponente.  <br/> |
   
## <a name="remarks"></a>Comentarios

Tanto el _número_ como el exponente pueden ser no enteros y pueden ser negativos. __ Si el _número_ no es 0 y el exponente es 0, esta función devuelve 1. __ Si el _número_ es 0 y el exponente es negativo, esta función devuelve 0,0. __ Si tanto el _número_ como el exponente son 0, o si el _número_ es negativo y el exponente no es un número entero, la función devuelve 0,0. __ __ Si tanto el _número_ como el exponente son negativos, esta función devuelve-1. #IND. __ 
  
## <a name="example"></a>Ejemplo

POW (5, 2) 
  
Devuelve 25. 
  

