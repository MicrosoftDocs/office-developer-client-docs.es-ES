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
description: Devuelve la subcadena en el índice de la ubicación de base cero de la lista delimitada por el delimitador. O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como el argumento valorDeError.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822329"
---
# <a name="index-function"></a>Función INDEX

Devuelve la subcadena en la ubicación de base cero _índice_ en la _lista_ delimitada por el _delimitador_. O bien, si el índice está fuera del intervalo, devuelve una cadena vacía o el token opcional proporcionado como el argumento *valorDeError* . 
  
## <a name="syntax"></a>Sintaxis

ÍNDICE (** *índice* **, "** *lista* **" [, [** *delimitador* **] [, [** *valorDeError* **]]]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatorio  <br/> |**Número** <br/> |Especifica la ubicación que desea buscar.  <br/> |
| _lista_ <br/> |Obligatorio  <br/> |**String** <br/> |Lista en la que desea realizar la búsqueda.  <br/> |
| _delimiter_ <br/> |Opcional  <br/> |**String** <br/> | La cadena que se utilizará como delimitador en _lista_. Una cadena _delimitador_ puede tener más de un carácter de longitud e incluir caracteres con múltiples bytes. El valor predeterminado es un punto y coma.  <br/> |
| _valorDeError_ <br/> |Opcional  <br/> |**Número** <br/> | Valor especificado por el usuario que debe devolverse en el caso de que el índice no esté incluido en el intervalo. El valor predeterminado es una cadena vacía.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si la lista comienza o termina con un delimitador, se supone que existe una cadena nula antes o después de la misma. Dos delimitadores consecutivos indican que hay una cadena nula entre ellos. 
  
Si el índice está fuera del intervalo, Visio devuelve una cadena vacía o el símbolo (token) opcional que el argumento *valorDeError* . 
  
## <a name="example-1"></a>Ejemplo 1

INDEX(3;"gato;rata;;cabra")
  
Devuelve "cabra".
  
## <a name="example-2"></a>Ejemplo 2

INDEX(54,";1;2;3;",,"ERROR")
  
Devuelve "ERROR".
  

