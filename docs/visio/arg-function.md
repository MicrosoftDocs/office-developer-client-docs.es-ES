---
title: ARG (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Especifica un argumento que la celda de llamada puede pasar a una función personalizada, así como el valor predeterminado devuelto por la función personalizada si la celda que llama no pasa un valor para el argumento. Devuelve el valor especificado por la celda que llama y el parámetro argName que coincide.
ms.openlocfilehash: 3cde7fe55d7bc60d15f32d7ad954443e545af914
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293488"
---
# <a name="arg-function"></a>Función ARG

Especifica un argumento que la celda de llamada puede pasar a una función personalizada, así como el valor predeterminado devuelto por la función personalizada si la celda que llama no pasa un valor para el argumento. Devuelve el valor especificado por la celda que llama y el parámetro argName que coincide.
  
## <a name="syntax"></a>Sintaxis

ARG(***argName***,[ ***defaultValue*** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _argName_ <br/> |Obligatorio  <br/> |**String** <br/> |Nombre de un argumento que la celda que realiza la llamada puede pasar a la función  <br/> |
| _valor predeterminado_ <br/> |Opcional  <br/> |**Numérico** <br/> |Valor devuelto por ARG si la celda que llama no pasó un valor para el _parámetro argName._  <br/> |
   
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


