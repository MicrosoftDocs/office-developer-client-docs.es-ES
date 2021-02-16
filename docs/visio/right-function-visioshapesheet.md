---
title: Función RIGHT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Devuelve el último carácter o caracteres de una cadena de texto, en función del número de caracteres que especifique.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411459"
---
# <a name="right-function-visioshapesheet"></a>Función RIGHT (VisioShapeSheet)

Devuelve el último carácter o caracteres de una cadena de texto, en función del número de caracteres que especifique.
  
## <a name="syntax"></a>Sintaxis

RIGHT(** *text* ** [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> | La cadena de texto que contiene los caracteres que se desea extraer.  <br/> |
| _num_chars_opt_ <br/> |Opcional  <br/> |**Number** <br/> |El número de caracteres que debe extraerse. El valor predeterminado es 1.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

El valor de  _num_chars_opt_ debe ser mayor o igual que cero (0). 
  
Si  _num_chars_opt_ mayor que la longitud del texto, RIGHT devuelve todo el texto. Si  _num_chars_opt_ se omite, se supone que es 1. 
  
## <a name="example"></a>Ejemplo

RIGHT ("1 de enero, 2004", 4) 
  
Devuelve el valor 2004. 
  

