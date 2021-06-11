---
title: Función MID (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Devuelve un número específico de caracteres de una cadena de texto, empezando por la posición que especifique, en función del número de caracteres que especifique.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410269"
---
# <a name="mid-function-visioshapesheet"></a>Función MID (VisioShapeSheet)

Devuelve un número específico de caracteres de una cadena de texto, empezando por la posición que especifique, en función del número de caracteres que especifique.
  
## <a name="syntax"></a>Sintaxis

MID (** *text* **, ** *start_num* **, ** *num_chars* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |La cadena de texto que contiene los caracteres que se desean extraer.  <br/> |
| _start_num_ <br/> |Obligatorio  <br/> |**Number** <br/> |La posición del primer carácter que se desea extraer. El primer carácter de la cadena de texto ocupa la posición 1.  <br/> |
| _num_chars_ <br/> |Obligatorio  <br/> |**Number** <br/> |El número de caracteres que debe devolverse.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Comentarios

Si  *start_num*  es: 
  
- Mayor que la longitud del  *texto,*  MID devuelve "" (texto vacío). 
    
- Menor que la longitud  *del*  texto, pero  *start_num*  más  *num_chars*  supera la longitud del texto  *,*  MID devuelve los caracteres hasta el final del  *texto*  . 
    
- Menor que 1, MID devuelve el error #VALUE! 
    
Si  *num_chars*  es negativo, MID devuelve el #VALUE! valor de error. 
  
## <a name="example"></a>Ejemplo

MID ("SSN 999-99-9999",5,11) 
  
Devuelve 999-99-9999. 
  

