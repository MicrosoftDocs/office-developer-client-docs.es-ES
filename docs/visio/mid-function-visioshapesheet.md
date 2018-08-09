---
title: MID (función) (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Devuelve un número específico de caracteres de una cadena de texto, empezando por la posición que especifique, en función del número de caracteres que especifique.
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822657"
---
# <a name="mid-function-visioshapesheet"></a>MID (función) (VisioShapeSheet)

Devuelve un número específico de caracteres de una cadena de texto, empezando por la posición que especifique, en función del número de caracteres que especifique.
  
## <a name="syntax"></a>Sintaxis

MID (** *texto* **, ** *número_inicio* **, ** *número_caracteres* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> |La cadena de texto que contiene los caracteres que se desean extraer.  <br/> |
| _número inicial_ <br/> |Obligatorio  <br/> |**Número** <br/> |La posición del primer carácter que se desea extraer. El primer carácter de la cadena de texto ocupa la posición 1.  <br/> |
| _número_caracteres_ <br/> |Obligatorio  <br/> |**Número** <br/> |Número de caracteres que se devuelve.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Notas

Si *número_inicio* es: 
  
- Mayor que la longitud del *texto* , MID devuelve "" (texto vacío). 
    
- Menor que la longitud del *texto* , pero la *suma de número_inicio* y *número_caracteres* excede la longitud del *texto* , MID devuelve los caracteres hasta el final del *texto* . 
    
- Menor que 1, MID devuelve el error #VALUE! 
    
¡Si *número_caracteres* es negativo, MID devuelve #VALUE! valor de error. 
  
## <a name="example"></a>Ejemplo

MID ("SSN 999-99-9999",5,11) 
  
Devuelve 999-99-9999. 
  

