---
title: EVALCELL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor para pasar a la función personalizada como argumentos (opcional). Devuelve el resultado calculado de la función personalizada a partir de los argumentos y valores especificados.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418907"
---
# <a name="evalcell-function"></a>Función EVALCELL

Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor para pasar a la función personalizada como argumentos (opcional). Devuelve el resultado calculado de la función personalizada a partir de los argumentos y valores especificados.
  
## <a name="syntax"></a>Sintaxis

EVALCELL (* * *cellRef* * *, [* * *arg1Name, arg1* * *], [* * *arg2Name, arg2* * *],...) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _referenciaDeCelda_ <br/> |Obligatorio  <br/> |**String** <br/> |Referencia a una celda que contiene la función personalizada. Se permiten referencias entre hojas.  <br/> |
| _arg1Name_ <br/> |Opcional  <br/> |**String** <br/> |Nombre del primer argumento que se va a pasar a la función personalizada. Se permiten espacios.  <br/> |
| _arg1_ <br/> |Opcional  <br/> |**Diferencias** <br/> |Valor del parámetro _arg1_ .  <br/> |
| _arg2Name_ <br/> |Opcional  <br/> |**String** <br/> |Nombre del segundo argumento que se va a pasar a la función personalizada. Se permiten espacios.  <br/> |
| _arg2_ <br/> |Opcional  <br/> |**Diferencias** <br/> |Valor del parámetro _arg2_ .  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Número
  
## <a name="remarks"></a>Comentarios

No es necesario especificar en la celda que realiza la llamada todos los argumentos utilizados por la función personalizada. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo utilizar la función EVALCELL en combinación con la función ARG para buscar el valor medio en un conjunto de tres valores. 
  
En la celda que contiene la expresión, coloque el código siguiente que define la función personalizada: 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

En las celdas que realizan la llamada, coloque el código siguiente que llama a la función personalizada:
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


