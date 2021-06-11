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
description: Determina si dos cadenas son las mismas.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413867"
---
# <a name="strsameex-function"></a>Función STRSAMEEX

Determina si dos cadenas son las mismas.
  
## <a name="syntax"></a>Sintaxis

STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera cadena de la comparación.  <br/> |
| _string2_ <br/> |Obligatorio  <br/> |**String** <br/> | La segunda cadena de la comparación.  <br/> |
| _localeID_ <br/> |Obligatorio  <br/> |**Numérico** <br/> |El código del identificador regional.  <br/> |
| _flag_ <br/> |Obligatorio  <br/> |**Numérico** <br/> | Un bit que especifica el tipo de comparación.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Comentarios

STRSAMEEX devuelve TRUE (verdadero) si son iguales y FALSE (falso) si no lo son. Use esta función para comparar cadenas de varios bytes o para hacer comparaciones usando reglas para una configuración local específica.
			

  
En la función STRSAMEEX, puede usar cualquier combinación de las siguientes marcas.
  
|**Flag**|**Descripción**|
|:-----|:-----|
|1  <br/> |No distinguir mayúsculas y minúsculas.  <br/> |
|2  <br/> |Omitir los caracteres que no ocupan un espacio.  <br/> |
|4   <br/> |Omitir los símbolos.  <br/> |
|4096  <br/> |Tratar la puntuación igual que los símbolos.  <br/> |
|65536  <br/> |No distinguir entre caracteres Hiragana y Katakana.  <br/> |
|131072  <br/> |No distinguir entre un carácter de un byte y el mismo como carácter de doble byte.  <br/> |
   

