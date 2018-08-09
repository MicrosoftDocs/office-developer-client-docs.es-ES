---
title: Al igual que (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Determina si una cadena de caracteres específica coincide con un patrón especificado. Un patrón puede incluir caracteres normales y caracteres comodín. Durante la coincidencia de patrones, los caracteres regulares deben coincidir exactamente con los caracteres especificados en la cadena de caracteres. Sin embargo, los caracteres comodín pueden coincidir con fragmentos arbitrarios de la cadena de caracteres. Uso de caracteres comodín hace que el operador LIKE sea más flexible que el uso de la = y! = operadores de comparación de cadena.
ms.openlocfilehash: d3224647c621b05a08bdc863939d0cccae214463
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815372"
---
# <a name="like-access-custom-web-app"></a>Al igual que (aplicación web personalizado de Access)

Determina si una cadena de caracteres específica coincide con un patrón especificado. Un patrón puede incluir caracteres normales y caracteres comodín. Durante la coincidencia de patrones, los caracteres regulares deben coincidir exactamente con los caracteres especificados en la cadena de caracteres. Sin embargo, los caracteres comodín pueden coincidir con fragmentos arbitrarios de la cadena de caracteres. Uso de caracteres comodín hace que el operador **LIKE** sea más flexible que el uso de la = y! = operadores de comparación de cadena. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *Expresión*  [NOT] **Al igual que** *Patrón*  [ESCAPE *EscapeChar* ] 
  
El operador **LIKE** contiene los siguientes argumentos 
  
|**Nombre del argumento**|**Necesario**|**Descripción**|
|:-----|:-----|:-----|
| *Expresión*  <br/> |Sí  <br/> |Una expresión válida.  <br/> |
| *Pattern*  <br/> |Sí  <br/> |La cadena específica de caracteres que se va a buscar en la *expresión* . Puede incluir caracteres comodín. Hacer referencia a los comentarios para obtener una lista de caracteres comodín válido.  <br/> |
| *EscapeChar*  <br/> |No  <br/> |Un carácter que se coloca delante de un carácter comodín para indicar que el carácter comodín se debe interpretar como un carácter normal y no como un carácter comodín.  *EscapeChar* es una expresión de caracteres que no tiene valor predeterminado y se debe evaluar como un solo carácter.  <br/> |
   
## <a name="remarks"></a>Comentarios

En la siguiente tabla contiene los caracteres comodín que son válidos para su uso en el argumento de *patrón* . 
  
|**Carácter comodín**|**Descripción**|**Ejemplo**|
|:-----|:-----|:-----|
|%  <br/> |Cualquier cadena de cero o más caracteres.  <br/> | *WHERE title LIKE '% computer %'* busca todos los títulos de los libros con la palabra 'computer' en cualquier lugar en el título del libro.  <br/> |
|_ (subrayado)  <br/> |Cualquier carácter único.  <br/> | *WHERE au_fname LIKE '_ean'* busca todos los nombres de la primera de cuatro letras que finalicen con ean (Dean, Juan y así sucesivamente).  <br/> |
|[]  <br/> |Cualquier un solo carácter dentro del intervalo especificado ([a-f]) o conjunto ([abcdef]).  <br/> | *WHERE au_lname LIKE '[C-p] arsen'* busca apellidos que terminan con arsen y comenzando con cualquier carácter individual entre C y P, por ejemplo Carsen, Larsen, Karsen, de autores y así sucesivamente.  <br/> |
|[^]  <br/> |Cualquier carácter individual no dentro del intervalo especificado ([^ a-f]) o conjunto ([^ abcdef]).  <br/> | *WHERE au_lname LIKE ' Excel [^ l] %'* todos los últimos nombres de y donde la letra siguiente no es l a partir de autor.  <br/> |
   
Cuando se realizan las comparaciones de cadenas mediante el uso de **como**, todos los caracteres en la cadena del modelo son importantes. Esto incluye espacios iniciales ni finales. Si es una comparación en una consulta para devolver todas las filas con una cadena **LIKE** 'abc' (abc seguido de un espacio), no se devuelve una fila en el que el valor de esa columna sea abc (abc sin un espacio). Sin embargo, los espacios en blanco, en la expresión a la que se compara el modelo, se omiten. Si es una comparación en una consulta para devolver todas las filas con la cadena **LIKE** 'abc' (abc sin un espacio), se devuelven todas las filas que comiencen con abc y tienen cero o más espacios en blanco finales. 
  
Si cualquiera de los argumentos no es del tipo de datos string, se convierte a un tipo de datos de cadena, si es posible.
  

