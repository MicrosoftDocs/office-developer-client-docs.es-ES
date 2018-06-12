---
title: STRSAMEEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Determina si dos cadenas son los mismos.
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823343"
---
# <a name="strsameex-function"></a>STRSAMEEX (función)

Determina si dos cadenas son los mismos.
  
## <a name="syntax"></a>Sintaxis

STRSAMEEX ("** *cadena1* **","** *cadena2* **", ** *localeID* **, ** *marca* **) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cadena1_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera cadena de la comparación.  <br/> |
| _cadena2_ <br/> |Obligatorio  <br/> |**String** <br/> | La segunda cadena de la comparación.  <br/> |
| _localeID_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El código del identificador regional.  <br/> |
| _marca_ <br/> |Obligatorio  <br/> |**Numérico** <br/> | Un bit que especifica el tipo de comparación.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Boolean
  
## <a name="remarks"></a>Notas

STRSAMEEX devuelve TRUE si ambas cadenas de entrada son los mismos y FALSE si no lo son. Utilice esta función para comparar cadenas de varios bytes o para hacer comparaciones que usan las reglas de mayúsculas y minúsculas para una configuración regional específica.
  
En la función STRSAMEEX, puede usar cualquier combinación de las siguientes marcas.
  
|**Flag**|**Descripción**|
|:-----|:-----|
|1  <br/> |No distinguir mayúsculas y minúsculas.  <br/> |
|2  <br/> |Omitir los caracteres que no ocupan un espacio.  <br/> |
|4  <br/> |Omitir los símbolos.  <br/> |
|4096  <br/> |Tratar la puntuación igual que los símbolos.  <br/> |
|65536  <br/> |No distinguir entre caracteres Hiragana y Katakana.  <br/> |
|131072  <br/> |No distinguir entre un carácter de un byte y el mismo como carácter de doble byte.  <br/> |
   

