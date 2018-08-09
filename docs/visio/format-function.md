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
description: Devuelve el resultado de expresión como una cadena con formato de acuerdo con el valor de formatoDeImagen.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822198"
---
# <a name="format-function"></a>Función FORMAT

Devuelve el resultado de _expresión_ como una cadena con formato de acuerdo con el _valor de formatoDeImagen_.
  
## <a name="syntax"></a>Sintaxis

FORMATO (** *expresión* **, "** *formatoDeImagen* **") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatorio  <br/> |**String** <br/> |Combinación de constantes, operadores, funciones y referencias a celdas de ShapeSheet que da como resultado un valor.  <br/> |
| _formatoDeImagen_ <br/> |Obligatorio  <br/> |**String** <br/> |La imagen de formato usada para dar formato a la cadena.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Notas

El tipo de la expresión y el tipo especificado en el formato de imagen controlan el comportamiento de la cadena devuelta. El _valor de formatoDeImagen_ debe ser adecuado para el tipo de expresión. Para obtener más información acerca de cómo especificar imágenes de formato, vea [acerca de las imágenes de formato](about-format-pictures.md).
  
Devuelve un error si el resultado de la _expresión_ y el tipo esperado en _formatoDeImagen_ son distintos, o si hay errores de sintaxis en _formatoDeImagen_.
  
## <a name="example-1"></a>Ejemplo 1

FORMAT(1cm/4, "0,000 u")
  
Devuelve "0,250 cm".
  
## <a name="example-2"></a>Ejemplo 2

FORMAT(1cm/4, "0,00 U")
  
Devuelve "0,25 CM".
  
## <a name="example-3"></a>Ejemplo 3

FORMAT(1cm/4, "0,0 u")
  
Devuelve "0,3 cm".
  

