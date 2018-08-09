---
title: Función de la derecha (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Devuelve el último carácter o caracteres de una cadena de texto, en función del número de caracteres que especifique.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822986"
---
# <a name="right-function-visioshapesheet"></a>Función de la derecha (VisioShapeSheet)

Devuelve el último carácter o caracteres de una cadena de texto, en función del número de caracteres que especifique.
  
## <a name="syntax"></a>Sintaxis

DERECHA (** *texto* ** [, ** *número_caracteres_opcional* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> | La cadena de texto que contiene los caracteres que se desea extraer.  <br/> |
| _número_caracteres_opcional_ <br/> |Opcional  <br/> |**Número** <br/> |El número de caracteres que debe extraerse. El valor predeterminado es 1.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Notas

El valor de _número_caracteres_opcional_ debe ser mayor o igual que cero (0). 
  
Si _número_caracteres_opcional_ es mayor que la longitud del texto, derecha devuelve todo el texto. Si se omite _número_caracteres_opcional_ , se supone que es 1. 
  
## <a name="example"></a>Ejemplo

RIGHT ("1 de enero, 2004", 4) 
  
Devuelve el valor 2004. 
  

