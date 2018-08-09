---
title: FIND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Busca una cadena de texto dentro de otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando con respecto a su posición en la cadena de texto que lo contiene.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822167"
---
# <a name="find-function"></a>Función FIND

Busca una cadena de texto dentro de otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando con respecto a su posición en la cadena de texto que lo contiene.
  
## <a name="syntax"></a>Sintaxis

Buscar (** *texto_buscado* **, ** *texto_continente* **, [** *número_inicio* **], [** *no_distinguir_mayúsculas_minúsculas* **]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _texto buscado_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto que desea buscar.  <br/> |
| _format_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto que contiene la cadena buscada.  <br/> |
| _número inicial_ <br/> |Opcional  <br/> |**Número** <br/> |El carácter en el que se va a iniciar la búsqueda. El primer carácter de _texto_continente_ es 1. Si _número_inicio_ es que faltan, se supone que es 1.  <br/> |
| _no_distinguir_mayúsculas_minúsculas_ <br/> |Opcional  <br/> |**Boolean** <br/> |De manera predeterminada, la función FIND distingue entre mayúsculas y minúsculas. Si desea que encuentre el texto sin diferenciar entre mayúsculas y minúsculas, establezca el argumento en TRUE.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Comentarios

Si se encuentran varias coincidencias, la función FIND devuelve la posición inicial de la primera coincidencia en la cadena. El argumento de _texto buscado_ no tiene en cuenta los caracteres comodines. 
  
Si _texto_buscado_:
  
-  Está vacío (""), FIND coincide con el primer carácter de la cadena de búsqueda (es decir, el carácter numeradas _número_inicio_ o 1). 
    
- ¡No aparece en _texto_continente_, devolverá #VALUE! valor de error. 
    
Si _número_inicio_:
  
- No es mayor que cero (0), devolverá el error #VALUE! 
    
- Es mayor que la longitud de _texto_continente_, devolverá #VALUE! valor de error. 
    
## <a name="example"></a>Ejemplo

FIND ("2003","1 de enero, 2003") 
  
Devuelve 12. 
  

