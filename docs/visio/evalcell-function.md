---
title: EVALCELL (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor que se pase a la función personalizada como argumentos (opcional). Devuelve el resultado de la función personalizada dados los argumentos especificados y los valores calculado.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822073"
---
# <a name="evalcell-function"></a>Función EVALCELL

Toma una referencia a una celda que contiene una función personalizada, así como uno o más pares de nombre y valor que se pase a la función personalizada como argumentos (opcional). Devuelve el resultado de la función personalizada dados los argumentos especificados y los valores calculado.
  
## <a name="syntax"></a>Sintaxis

EVALCELL (** *cellRef* **, [** *arg1Name, arg1* **], [** *arg2Name, arg2* **], …) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _cellRef_ <br/> |Obligatorio  <br/> |**String** <br/> |Una referencia a la celda que contiene la función personalizada. Se permiten referencias entre hojas.  <br/> |
| _arg1Name_ <br/> |Opcional  <br/> |**String** <br/> |Nombre del primer argumento que se va a pasar a la función personalizada. Se permiten espacios.  <br/> |
| _Arg1_ <br/> |Opcional  <br/> |**Varían** <br/> |Valor del parámetro _arg1_ .  <br/> |
| _arg2Name_ <br/> |Opcional  <br/> |**String** <br/> |El nombre del segundo argumento que se pasan a la función personalizada. Se permiten espacios.  <br/> |
| _Arg2_ <br/> |Opcional  <br/> |**Varían** <br/> |Valor del parámetro _arg2_ .  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Number
  
## <a name="remarks"></a>Observaciones

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


