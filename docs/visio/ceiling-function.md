---
title: CEILING (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Redondear un número de 0 (cero) a la siguiente instancia de múltiplo. Si no se especifica multiple, el número se redondea de 0 al siguiente entero.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404130"
---
# <a name="ceiling-function"></a>Función CEILING

Redondea un número de 0 (cero) a la siguiente instancia de  _varios_. Si  _no_ se especifica multiple, el número se redondea de 0 al siguiente entero. 
  
## <a name="syntax"></a>Sintaxis

CEILING(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número que desea redondear.  <br/> |
| _multiple_ <br/> |Obligatorio  <br/> |**Number** <br/> |Múltiplo al que redondear.  <br/> |
   
## <a name="remarks"></a>Comentarios

 _El_ número  _y el_ múltiplo deben tener los mismos signos o un #NUM! se devuelve. Si no  _se_  _puede_ convertir un número o varios en un valor, #VALUE! se devuelve. Si el  _número_ o  _múltiplo_ es 0, el resultado es 0. 
  
## <a name="example-1"></a>Ejemplo 1

CEILING(3.7)
  
Devuelve 4.
  
## <a name="example-2"></a>Ejemplo 2

CEILING(-3.7)
  
Devuelve -4.
  
## <a name="example-3"></a>Ejemplo 3

CEILING(3.7, 0.25)
  
Devuelve 3,75.
  

