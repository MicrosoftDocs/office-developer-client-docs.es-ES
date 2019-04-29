---
title: LOOKUP (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Devuelve un índice basado en cero que indica la ubicación de la clave de subcadena en una lista o devuelve-1 si la cadena de destino contiene el delimitador.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410332"
---
# <a name="lookup-function"></a>Función LOOKUP

Devuelve un índice basado en cero que indica la ubicación de la _clave_ de subcadena en una _lista_o devuelve-1 si la cadena de destino contiene __ el delimitador.
  
## <a name="syntax"></a>Sintaxis

Lookup ("* * *key* * *", "* * *List* * *" [, "* * ** delimitador * *"]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _key_ <br/> |Obligatorio  <br/> |**String** <br/> |Cadena que desea buscar.  <br/> |
| _list_ <br/> |Obligatorio  <br/> |**String** <br/> | Lista en la que desea realizar la búsqueda.  <br/> |
| _delimiter_ <br/> |Opcional  <br/> |**String** <br/> | La cadena que se va a usar como delimitador de la _lista_. Una __ cadena de delimitador puede tener más de un carácter de longitud y puede incluir caracteres de varios bytes. El valor predeterminado es un punto y coma.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numérico
  
## <a name="remarks"></a>Comentarios

La función LOOKUP utiliza un sistema de búsqueda que no diferencia mayúsculas y minúsculas. Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos. 
  
Todos los argumentos deben ser cadenas o expresiones que se puedan convertir en cadenas. En caso contrario, el argumento que no cumpla esa norma será reemplazado por una cadena nula. 
  
## <a name="example-1"></a>Ejemplo 1

LOOKUP ("rata", "gato; rata;; caprino ")
  
Devuelve 1.
  
## <a name="example-2"></a>Ejemplo 2

BÚSQUEDA ("", "; cat; Rat;; caprino ")
  
Devuelve 0.
  
## <a name="example-3"></a>Ejemplo 3

LOOKUP ("t", "gato; Rat;; caprino "," a ")
  
Devuelve 3.
  

