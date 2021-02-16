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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406314"
---
# <a name="pow-function"></a>Función POW

Devuelve un número elevado a la potencia de un exponente.
  
## <a name="syntax"></a>Sintaxis

POW(** *number* **, ** *exponent* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número para elevar la potencia del exponente.  <br/> |
| _exponent_ <br/> |Obligatorio  <br/> |**Number** <br/> |El exponente.  <br/> |
   
## <a name="remarks"></a>Comentarios

Tanto  _el número_ como el  _exponente_ pueden no ser enteros y pueden ser negativos. Si  _el_ número no es 0 y  _el exponente_ es 0, esta función devuelve 1. Si  _el_ número es 0 y  _el exponente_ es negativo, esta función devuelve 0,0. Si el _número_ y _el exponente_ son 0, o si el número es negativo y el _exponente_ no es un entero, esta función devuelve 0,0.  Si el  _número_ y  _el exponente_ son negativos, esta función devuelve -1,#IND. 
  
## <a name="example"></a>Ejemplo

POW(5,2) 
  
Devuelve 25. 
  

