---
title: SUBSTITUTE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Reemplaza parte de una cadena de texto por una cadena de texto diferente.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346826"
---
# <a name="substitute-function"></a>Función SUBSTITUTE

Reemplaza parte de una cadena de texto por una cadena de texto diferente. 
  
## <a name="syntax"></a>Sintaxis

 Substitute (* * *Text* * *, * * *texto_original* * *, * * *texto_nuevo* * * [, * * *núm_inicial* * *] [, * * *ignore_case_opt* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> | El texto o la referencia a la celda que contiene el texto cuyos caracteres se desea reemplazar.  <br/> |
| _texto_original_ <br/> |Obligatorio  <br/> |**String** <br/> | El texto que se desea reemplazar.  <br/> |
| _argumento_ <br/> |Obligatorio  <br/> |**String** <br/> | Texto que se va a usar para reemplazar _texto_original_.  <br/> |
| _start_num_opt_ <br/> |Opcional  <br/> |**Numeric** <br/> |Especifica qué ocurrencias de texto_original se reemplazarán.  <br/> |
| _ignore_case_opt_ <br/> |Opcional  <br/> |**Boolean** <br/> |Será FALSE si diferencia entre mayúsculas y minúsculas y, si no, TRUE. El valor predeterminado es FALSE (falso).  <br/> |
   
### <a name="return-value"></a>Valor devuelto

String
  
## <a name="remarks"></a>Comentarios

 Si especifica _start_num_opt_, solo se reemplazará esa aparición de _texto_original_ . De lo contrario, todas las apariciones de _texto_original_ en _texto_ se cambian a _texto_nuevo._
  
Use esta función cuando desee reemplazar un texto específico dentro de una cadena de texto. Si desea reemplazar el texto que aparece en una ubicación específica de una cadena de texto, use la función rePLACE.
  
## <a name="example"></a>Ejemplo

SUBSTITUTE ("1 de enero, 2003", "de enero,", "ene") 
  
Devuelve "1 ene 2003". 
  
SUBSTITUTE ("1 de enero, 2003","de Enero,","ene") 
  
Devuelve "1 de enero, 2003". No se modifica la cadena porque la búsqueda distingue entre mayúsculas y minúsculas. 
  

