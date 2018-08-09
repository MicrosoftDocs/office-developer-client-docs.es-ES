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
description: Determina si las cadenas son los mismos. Devuelve TRUE si son iguales y FALSE si no lo son.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823321"
---
# <a name="strsame-function"></a>Función STRSAME

Determina si las cadenas son los mismos. Devuelve TRUE si son iguales y FALSE si no lo son. 
  
## <a name="syntax"></a>Sintaxis

STRSAME ("** *cadena1* **","** *cadena2* **", ** *ignoreCase* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cadena1_ <br/> |Obligatorio  <br/> |**String** <br/> |La primera cadena de la comparación.  <br/> |
| _cadena2_ <br/> |Obligatorio  <br/> |**String** <br/> |La segunda cadena de la comparación.  <br/> |
| _ignoreCase_ <br/> |Opcional  <br/> |**Boolean** <br/> |TRUE (verdadero) para no distinguir mayúsculas y minúsculas y FALSE (falso) para hacerlo. El valor predeterminado es FALSE.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Booleano
  
## <a name="remarks"></a>Observaciones

Para comparar cadenas de varios bytes o para hacer comparaciones utilizando reglas para una configuración local específica, use la función STRSAMEEX.
  
## <a name="example-1"></a>Ejemplo 1

STRSAME("gato","perro")
  
Devuelve FALSE.
  
## <a name="example-2"></a>Ejemplo 2

STRSAME("gato","gato")
  
Devuelve TRUE.
  
## <a name="example-3"></a>Ejemplo 3

STRSAME("gato","gato", TRUE)
  
Devuelve TRUE.
  
## <a name="example-4"></a>Ejemplo 4

STRSAME("gato","GATO")
  
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
  

