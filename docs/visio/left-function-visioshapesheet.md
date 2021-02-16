---
title: Función LEFT (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Devuelve el carácter o los caracteres más a la izquierda de una cadena de texto, en función del número de caracteres que especifique.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427524"
---
# <a name="left-function-visioshapesheet"></a>Función LEFT (VisioShapeSheet)

Devuelve el carácter o los caracteres más a la izquierda de una cadena de texto, en función del número de caracteres que especifique.
  
## <a name="syntax"></a>Sintaxis

LEFT(** *text* **, [, ** *num_chars_opt* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |La cadena de texto que contiene los caracteres que se desean extraer.  <br/> |
| _num_chars_opt_ <br/> |Opcional  <br/> |**Numérico** <br/> |El número de caracteres que debe extraerse.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

El valor de  _num_chars_opt_ debe ser mayor o igual que cero (0). 
  
Si  _num_chars_opt_ mayor que la longitud del texto, LEFT devuelve todo el texto. Si  _num_chars_opt_ se omite, se supone que es 1. 
  
## <a name="example"></a>Ejemplo

LEFT ("Enero 1, 2004", 3) 
  
Devuelve el valor "Ene". 
  

