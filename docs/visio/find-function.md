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
description: Busca una cadena de texto contenida en otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando en relación con su posición en la cadena de texto que la contiene.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426579"
---
# <a name="find-function"></a>Función FIND

Busca una cadena de texto contenida en otra cadena de texto y devuelve la posición inicial de la cadena de texto que está buscando en relación con su posición en la cadena de texto que la contiene.
  
## <a name="syntax"></a>Sintaxis

FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _find_text_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto que desea buscar.  <br/> |
| _format_ <br/> |Obligatorio  <br/> |**String** <br/> |El texto que contiene la cadena buscada.  <br/> |
| _start_num_ <br/> |Opcional  <br/> |**Number** <br/> |El carácter por el cual se empezará la búsqueda. El primer carácter de  _within_text_ es 1. Si  _start_num_ falta, se supone que es 1.  <br/> |
| _ignore_case_ <br/> |Opcional  <br/> |**Boolean** <br/> |De manera predeterminada, la función FIND distingue entre mayúsculas y minúsculas. Si desea que encuentre el texto sin diferenciar entre mayúsculas y minúsculas, establezca el argumento en TRUE.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

Si se encuentra el texto varias veces, la función FIND devolverá la posición de inicio de la primera aparición en la cadena. El  _find_text_ no considera que ningún carácter sea comodín. 
  
Si _find_text:_
  
-  Está vacío (""), FIND coincide con el primer carácter de la cadena de búsqueda (es decir, el carácter  _numerado start_num_ o 1). 
    
- No aparece en  _within_text_, FIND devuelve el #VALUE! valor de error. 
    
Si _start_num:_
  
- No es mayor que cero (0), FIND devuelve el #VALUE! valor de error. 
    
- Es mayor que la longitud de  _within_text_, FINDreturns el #VALUE! valor de error. 
    
## <a name="example"></a>Ejemplo

FIND ("2003","1 de enero, 2003") 
  
Devuelve 12. 
  

