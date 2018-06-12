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
description: Reemplaza parte de una cadena de texto con una cadena de texto diferente.
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823347"
---
# <a name="substitute-function"></a>SUBSTITUTE (función)

Reemplaza parte de una cadena de texto con una cadena de texto diferente. 
  
## <a name="syntax"></a>Sintaxis

 SUBSTITUTE (** *texto* **, ** *texto_anterior* **, ** *texto_nuevo* ** [, ** *número_inicio* **] [, ** *distinguir_mayúsculas_minúsculas_opcional* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Obligatorio  <br/> |**String** <br/> | El texto o la referencia a la celda que contiene el texto cuyos caracteres se desea reemplazar.  <br/> |
| _texto original_ <br/> |Obligatorio  <br/> |**String** <br/> | El texto que desea reemplazar.  <br/> |
| _texto_nuevo_ <br/> |Obligatorio  <br/> |**String** <br/> | El texto que desea usar para reemplazar el _texto original_.  <br/> |
| _número_inicio_opcional_ <br/> |Opcional  <br/> |**Numérico** <br/> |Especifica qué apariciones de texto_anterior desea reemplazar.  <br/> |
| _distinguir_mayúsculas_minúsculas_opcional_ <br/> |Opcional  <br/> |**Boolean** <br/> |Será FALSE si diferencia entre mayúsculas y minúsculas y, si no, TRUE. El valor predeterminado es FALSE (falso).  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Cadena
  
## <a name="remarks"></a>Notas

 Si especifica _número_inicio_opcional_, se reemplaza la única aparición de _texto_anterior_ . De lo contrario, todas las apariciones de _texto_anterior_ en _texto_ se ha cambiado a _texto_nuevo._
  
Utilice la función sustituir cuando desee reemplazar texto específico en una cadena de texto. Si desea reemplazar el texto que se produce en una ubicación específica en una cadena de texto, use la función REPLACE.
  
## <a name="example"></a>Ejemplo

SUBSTITUTE ("1 de enero, 2003", "de enero,", "ene") 
  
Devuelve "1 ene 2003". 
  
SUBSTITUTE ("1 de enero, 2003","de Enero,","ene") 
  
Devuelve "1 de enero de 2003". No hay cambios debido a que la búsqueda de texto distingue mayúsculas de minúsculas. 
  

