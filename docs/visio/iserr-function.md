---
title: ISERR (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Devuelve TRUE si el valor de cellreference es cualquier tipo de error excepto #N/A; de lo contrario, devuelve FALSE. La función ISERR se usa en fórmulas que hacen referencia a otra celda.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432110"
---
# <a name="iserr-function"></a>Función ISERR

Devuelve TRUE si el valor de  _cellreference_ es cualquier tipo de error excepto #N/A; de lo contrario, devuelve FALSE. La función ISERR se usa en fórmulas que hacen referencia a otra celda. 
  
## <a name="syntax"></a>Sintaxis

ISERR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda.  <br/> |
   
## <a name="example-1"></a>Ejemplo 1

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.A1)  <br/> |FALSE  <br/> |
   
Devuelve FALSE ya que #N/A! es un error que la función ISERR no reconoce. Utilice ISERROR para encontrar todos los tipos de errores.
  
## <a name="example-2"></a>Ejemplo 2

|**Cell**|**Formula**|**Valor devuelto**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Devuelve TRUE ya que #VALUE! es un error que la función ISERR reconoce.
  

