---
title: INDEX (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Devuelve la subcadena en el índice de ubicación de base cero de la lista delimitada por delimitador. O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como argumento de valor de error.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431578"
---
# <a name="index-function"></a>Función INDEX

Devuelve la subcadena en  el índice de ubicación de base cero de la _lista_ delimitada _por delimitador_. O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como argumento *errorvalue.* 
  
## <a name="syntax"></a>Sintaxis

INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatorio  <br/> |**Number** <br/> |Especifica la ubicación que desea buscar.  <br/> |
| _list_ <br/> |Obligatorio  <br/> |**String** <br/> |Lista en la que desea realizar la búsqueda.  <br/> |
| _delimiter_ <br/> |Opcional  <br/> |**String** <br/> | La cadena que se usará como delimitador dentro de la  _lista_. Una  _cadena delimitadora_ puede tener más de un carácter de longitud e incluir caracteres multibyte. El valor predeterminado es un punto y coma.  <br/> |
| _errorvalue_ <br/> |Opcional  <br/> |**Number** <br/> | Valor especificado por el usuario que debe devolverse en el caso de que el índice no esté incluido en el intervalo. El valor predeterminado es una cadena vacía.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos. 
  
Si el índice está fuera del intervalo, Visio devuelve una cadena vacía o el token opcional proporcionado como argumento  *de valor de*  error. 
  
## <a name="example-1"></a>Ejemplo 1

INDEX(3,"cat;rat;; indeste")
  
Devuelve "cabra".
  
## <a name="example-2"></a>Ejemplo 2

INDEX(54,";1;2;3;","ERROR")
  
Devuelve "ERROR".
  

