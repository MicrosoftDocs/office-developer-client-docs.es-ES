---
title: STRSAME (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Determina si las cadenas son iguales. Devuelve TRUE si son iguales y FALSE si no lo son.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428686"
---
# <a name="strsame-function"></a>Función STRSAME

Determina si las cadenas son iguales. Devuelve TRUE si son iguales y FALSE si no lo son. 
  
## <a name="syntax"></a>Sintaxis

STRSAME ("* * *string1* * *", "* * *cadena2* * *", * * *ignoreCase* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera cadena de la comparación.  <br/> |
| _string2_ <br/> |Obligatorio  <br/> |**String** <br/> |La segunda cadena de la comparación.  <br/> |
| _ignoreCase_ <br/> |Opcional  <br/> |**Boolean** <br/> |TRUE (verdadero) para no distinguir mayúsculas y minúsculas y FALSE (falso) para hacerlo. El valor predeterminado es FALSE.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Comentarios

Para comparar cadenas de varios bytes o para hacer comparaciones utilizando reglas para una configuración local específica, use la función STRSAMEEX.
  
## <a name="example-1"></a>Ejemplo 1

STRSAME ("gato", "perro")
  
Devuelve FALSE.
  
## <a name="example-2"></a>Ejemplo 2

STRSAME ("gato", "gato")
  
Devuelve TRUE.
  
## <a name="example-3"></a>Ejemplo 3

STRSAME("gato","gato", TRUE)
  
Devuelve TRUE.
  
## <a name="example-4"></a>Ejemplo 4

STRSAME ("gato", "gato")
  
Devuelve FALSE.
  
## <a name="example-5"></a>Ejemplo 5

STRSAME("gato","GATO", TRUE)
  
Devuelve TRUE.
  
## <a name="example-6"></a>Ejemplo 6

STRSAME("gäto,"GATO", TRUE)
  
Devuelve FALSE.
  
## <a name="example-7"></a>Ejemplo 7

STRSAME("gäto,"GÄTO", TRUE)
  
Devuelve TRUE.
  

