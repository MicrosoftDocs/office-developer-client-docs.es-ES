---
title: FORMAT (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Devuelve el resultado de la expresión como una cadena con formato de acuerdo con formatodeimagen.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339896"
---
# <a name="format-function"></a>Función FORMAT

Devuelve el resultado de la _expresión_ como una cadena con formato de acuerdo con _formatodeimagen_.
  
## <a name="syntax"></a>Sintaxis

Format (* * *expresión* * *, "* * *formatodeimagen* * *") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.  <br/> |
| _formatodeimagen_ <br/> |Obligatorio  <br/> |**String** <br/> |La imagen de formato usada para dar formato a la cadena.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

El tipo de la expresión y el especificado en el formato de imagen controlan el comportamiento de la cadena devuelta. _Formatodeimagen_ debe ser adecuado para el tipo de expresión. Para obtener más información acerca de cómo especificar imágenes de formato, vea [acerca de las imágenes de formato](about-format-pictures.md).
  
Devuelve un error si el resultado de la _expresión_ y el tipo esperado en _formatodeimagen_ son de diferente tipo o si hay errores de sintaxis en _formatodeimagen_.
  
## <a name="example-1"></a>Ejemplo 1

FORMAT(1cm/4, "0,000 u")
  
Devuelve "0,250 cm".
  
## <a name="example-2"></a>Ejemplo 2

FORMAT(1cm/4, "0,00 U")
  
Devuelve "0,25 CM".
  
## <a name="example-3"></a>Ejemplo 3

FORMAT(1cm/4, "0,0 u")
  
Devuelve "0,3 cm".
  

