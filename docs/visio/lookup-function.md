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
description: Devuelve un índice de base cero que indica la ubicación de la subcadena clave en una lista o devuelve -1 si la cadena de destino contiene el delimitador.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822554"
---
# <a name="lookup-function"></a>LOOKUP (función)

Devuelve un índice de base cero que indica la ubicación de la subcadena _clave_ en una _lista_o devuelve -1 si la cadena de destino contiene el _delimitador_.
  
## <a name="syntax"></a>Sintaxis

BÚSQUEDA ("** *clave* **","** *lista* **"["," ** *delimitador* ** "]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _clave_ <br/> |Obligatorio  <br/> |**String** <br/> |Cadena que desea buscar.  <br/> |
| _lista_ <br/> |Obligatorio  <br/> |**String** <br/> | Lista en la que desea realizar la búsqueda.  <br/> |
| _delimiter_ <br/> |Opcional  <br/> |**String** <br/> | La cadena que se utilizará como delimitador en _lista_. Una cadena _delimitador_ puede tener más de un carácter de longitud y puede incluir caracteres con múltiples bytes. El valor predeterminado es un punto y coma.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Numeric
  
## <a name="remarks"></a>Observaciones

La función LOOKUP utiliza un sistema de búsqueda que no diferencia mayúsculas y minúsculas. Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos. 
  
Todos los argumentos deben ser cadenas o expresiones que se puedan convertir en cadenas. En caso contrario, el argumento que no cumpla esa norma será reemplazado por una cadena nula. 
  
## <a name="example-1"></a>Ejemplo 1

LOOKUP("rata","gato;rata;;cabra")
  
Devuelve 1.
  
## <a name="example-2"></a>Ejemplo 2

LOOKUP("";";gato;rata;;cabra")
  
Devuelve 0.
  
## <a name="example-3"></a>Ejemplo 3

LOOKUP("t","gato;rata;;pato","a")
  
Devuelve 3.
  

