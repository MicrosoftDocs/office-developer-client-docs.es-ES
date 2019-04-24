---
title: ARG (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Especifica un argumento que la celda que realiza la llamada puede pasar a una función personalizada, así como el valor predeterminado devuelto por la función personalizada si la celda que realiza la llamada no pasa un valor para el argumento. Devuelve el valor especificado por la celda que realiza la llamada y el parámetro argName correspondiente.
ms.openlocfilehash: f85c3dc4a49878b034674330f272a63e79c17d49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341436"
---
# <a name="arg-function"></a>Función ARG

Especifica un argumento que la celda que realiza la llamada puede pasar a una función personalizada, así como el valor predeterminado devuelto por la función personalizada si la celda que realiza la llamada no pasa un valor para el argumento. Devuelve el valor especificado por la celda que realiza la llamada y el parámetro argName correspondiente.
  
## <a name="syntax"></a>Sintaxis

Arg (* * *argName* * *, [* * *DefaultValue* * *]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |Obligatorio  <br/> |**String** <br/> |Nombre de un argumento que la celda que realiza la llamada puede pasar a la función  <br/> |
| _Valor predeterminado_ <br/> |Opcional  <br/> |**Numeric** <br/> |El valor devuelto por ARG si la celda que realiza la llamada no pasa un valor para el parámetro _argName_ .  <br/> |
   
## <a name="remarks"></a>Comentarios

Como programador de formas, puede crear funciones personalizadas colocando una expresión en una celda y llamando a esa expresión desde una o varias celdas. Esta expresión puede incluir cadenas literales y funciones y referencias a celdas de ShapeSheet. Esta expresión también puede incluir argumentos específicos que pasa la celda que realiza la llamada. 
  
La celda que realiza la llamada especifica la celda que contiene la función personalizada, así como los argumentos que desea pasar a la función. La celda que contiene la expresión se evalúa y se devuelve el resultado a la celda que realiza la llamada.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo utilizar la función ARG en combinación con la función EVALCELL para buscar el valor medio en un conjunto de tres valores. 
  
En la celda que contiene la expresión, coloque el código siguiente que define la función personalizada: 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

En las celdas que realizan la llamada, coloque el código siguiente que llama a la función personalizada:
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


