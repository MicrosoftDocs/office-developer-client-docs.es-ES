---
title: LIKE (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Determina si una cadena de caracteres específica coincide con un patrón especificado. Un patrón puede incluir caracteres normales y caracteres comodín. Durante la coincidencia de patrones, los caracteres normales deben coincidir exactamente con los caracteres especificados en la cadena de caracteres. Sin embargo, los caracteres comodín pueden coincidir con fragmentos arbitrarios de la cadena de caracteres. El uso de caracteres comodín hace que el operador LIKE sea más flexible que el uso de los operadores de comparación de cadenas = y! =.
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406118"
---
# <a name="like-access-custom-web-app"></a>LIKE (aplicación web personalizada de Access)

Determina si una cadena de caracteres específica coincide con un patrón especificado. Un patrón puede incluir caracteres normales y caracteres comodín. Durante la coincidencia de patrones, los caracteres normales deben coincidir exactamente con los caracteres especificados en la cadena de caracteres. Sin embargo, los caracteres comodín pueden coincidir con fragmentos arbitrarios de la cadena de caracteres. El uso de caracteres comodín hace que el operador **like** sea más flexible que el uso de los operadores de comparación de cadenas = y! =. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *Expresión*  NO **Como** *Patrón*  [ESCAPE *EscapeChar* ] 
  
El operador **like** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
| *Expression*  <br/> |Sí  <br/> |Una expresión válida.  <br/> |
| *Pattern*  <br/> |Sí  <br/> |La cadena de caracteres específica que se va a buscar en la *expresión* . Puede incluir caracteres comodín. Consulte las notas para obtener una lista de caracteres comodín válidos.  <br/> |
| *EscapeChar*  <br/> |No  <br/> |Un carácter que se coloca delante de un carácter comodín para indicar que el comodín debe interpretarse como un carácter normal y no como un comodín.  *EscapeChar* es una expresión de caracteres que no tiene valor predeterminado y debe evaluarse como un solo carácter.  <br/> |
   
## <a name="remarks"></a>Comentarios

La siguiente tabla contiene los caracteres comodín que son válidos para su uso en el argumento *Pattern* . 
  
|**Carácter comodín**|**Descripción**|**Ejemplo**|
|:-----|:-----|:-----|
|%  <br/> |Cualquier cadena de cero o más caracteres.  <br/> | *Donde título como '% equipo% '* busca todos los títulos de los libros con la palabra ' equipo ' en cualquier lugar del título del libro.  <br/> |
|_ (subrayado)  <br/> |Cualquier carácter único.  <br/> | *Donde AU_FNAME like ' _ean '* busca todos los nombres de cuatro letras que terminan con EAN (Dean, Juan, etc.).  <br/> |
|[]  <br/> |Cualquier carácter individual dentro del intervalo especificado ([a-f]) o set ([abcdef]).  <br/> | *Donde AU_LNAME like ' [C-P] Arsen '* busca los apellidos del autor que acaben con Arsen y empiecen con cualquier carácter único entre C y P, por ejemplo Carsen, Larsen, Karsen y así sucesivamente.  <br/> |
|[^]  <br/> |Cualquier carácter único que no se encuentre en el intervalo especificado ([^ a-f]) o set ([^ abcdef]).  <br/> | *Donde AU_LNAME like ' de [^ l]% '* son todos los apellidos de autor que comienzan con el y donde la siguiente letra no es l.  <br/> |
   
Cuando se realizan comparaciones de cadenas mediante **like**, todos los caracteres de la cadena de patrón son significativos. Esto incluye espacios iniciales o finales. Si una comparación en una consulta es devolver todas las filas con una cadena **como** ' ABC ' (ABC seguido de un espacio), no se devuelve una fila en la que el valor de esa columna es ABC (ABC sin un espacio). Sin embargo, se omiten los espacios en blanco al final, en la expresión en la que se compara el patrón. Si una comparación en una consulta es devolver todas las filas con la cadena **like** ' ABC ' (ABC sin un espacio), se devuelven todas las filas que comienzan con ABC y tienen cero o más espacios en blanco a la derecha. 
  
Si alguno de los argumentos no es del tipo de datos String, se convierte en un tipo de datos String, si es posible.
  

