---
title: LIKE (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: Determina si una cadena de caracteres específica coincide con un patrón especificado. Un patrón puede incluir caracteres normales y caracteres comodín. Durante la coincidencia de tramas, los caracteres normales deben coincidir exactamente con los caracteres especificados en la cadena de caracteres. Sin embargo, los caracteres comodín pueden coincidir con fragmentos arbitrarios de la cadena de caracteres. El uso de caracteres comodín hace que el operador LIKE sea más flexible que usar los operadores de comparación de cadena = y !=.
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406118"
---
# <a name="like-access-custom-web-app"></a>LIKE (aplicación web personalizada de Access)

Determina si una cadena de caracteres específica coincide con un patrón especificado. Un patrón puede incluir caracteres normales y caracteres comodín. Durante la coincidencia de tramas, los caracteres normales deben coincidir exactamente con los caracteres especificados en la cadena de caracteres. Sin embargo, los caracteres comodín pueden coincidir con fragmentos arbitrarios de la cadena de caracteres. El uso de caracteres comodín hace que el operador **LIKE** sea más flexible que usar los operadores de comparación de cadena = y !=. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 *Expresión*  [ NOT ] **Patrón LIKE** *[*  ESCAPE  *EscapeChar*  ] 
  
El **operador LIKE** contiene los argumentos siguientes 
  
|**Nombre de argumento**|**Obligatorio**|**Descripción**|
|:-----|:-----|:-----|
| *Expression*  <br/> |Sí  <br/> |Expresión válida.  <br/> |
| *Pattern*  <br/> |Sí  <br/> |La cadena de caracteres específica que se debe buscar en  *Expression*  . Puede incluir caracteres comodín. Consulte los comentarios para obtener una lista de caracteres comodín válidos.  <br/> |
| *EscapeChar*  <br/> |No  <br/> |Carácter que se coloca delante de un carácter comodín para indicar que el carácter comodín debe interpretarse como un carácter normal y no como un carácter comodín.  *EscapeChar*  es una expresión de carácter que no tiene ningún valor predeterminado y debe evaluarse como un solo carácter.  <br/> |
   
## <a name="remarks"></a>Comentarios

La tabla siguiente contiene los caracteres comodín que son válidos para su uso en el *argumento Pattern.* 
  
|**Carácter comodín**|**Descripción**|**Ejemplo**|
|:-----|:-----|:-----|
|%  <br/> |Cualquier cadena de cero o más caracteres.  <br/> | *WHERE title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title.  <br/> |
|_ (subrayado)  <br/> |Cualquier carácter único.  <br/> | *WHERE au_fname LIKE '_ean'*  busca todos los nombres de cuatro letras que terminan con ean (Dean, Sean, entre otros).  <br/> |
|[]  <br/> |Cualquier carácter único dentro del intervalo especificado ([a-f]) o establecido ([abcdef]).  <br/> | *WHERE au_lname LIKE '[C-P]arsen'*  encuentra los apellidos de autor que terminan con arsen y comienzan con cualquier carácter único entre C y P, por ejemplo, Carsen, Larsen, Karsen, y así sucesivamente.  <br/> |
|[^]  <br/> |Cualquier carácter único que no se encuentra dentro del intervalo especificado ([^a-f]) o establecido ([^abcdef]).  <br/> | *WHERE au_lname LIKE 'de[^l]%'*  todos los apellidos de autor empezando por de y donde la letra siguiente no es l.  <br/> |
   
Cuando se realizan comparaciones de cadenas mediante **LIKE**, todos los caracteres de la cadena de patrón son significativos. Esto incluye espacios iniciales o finales. Si una comparación de una consulta es devolver todas las filas con una cadena **LIKE** 'abc' (abc seguido de un único espacio), no se devuelve una fila en la que el valor de esa columna es abc (abc sin espacio). Sin embargo, se omiten los espacios en blanco finales, en la expresión con la que coincide el patrón. Si una comparación en una consulta es devolver todas las filas con la cadena **LIKE** 'abc' (abc sin espacio), se devuelven todas las filas que comienzan por abc y tienen cero o más espacios en blanco finales. 
  
Si alguno de los argumentos no es de un tipo de datos de cadena, se convierte en un tipo de datos de cadena, si es posible.
  

