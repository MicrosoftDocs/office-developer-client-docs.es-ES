---
title: Operadores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251824
localization_priority: Normal
ms.assetid: 43128ea2-c0d9-c45f-31e6-768a80ae59b2
description: Puede utilizar operadores en las fórmulas para realizar operaciones aritméticas (suma, resta, multiplicación, etc.) o comparaciones lógicas (mayor que, menor que, igual a, etc.). También puede controlar el orden en que se evalúan los términos de una fórmula mediante el uso de paréntesis. Utilice el operador & para combinar (concatenar) cadenas de caracteres.
ms.openlocfilehash: 4f095df73f9bd1d6a876d975d262c9217c696fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406132"
---
# <a name="about-operators"></a>Operadores

Puede utilizar operadores en las fórmulas para realizar operaciones aritméticas (suma, resta, multiplicación, etc.) o comparaciones lógicas (mayor que, menor que, igual a, etc.). También puede controlar el orden en que se evalúan los términos de una fórmula mediante el uso de paréntesis. Utilice el operador & para combinar (concatenar) cadenas de caracteres.
  
Microsoft Visio intenta convertir automáticamente los tipos de datos cuando una operación o función requiere un tipo específico. Por ejemplo, el operador de multiplicación requiere argumentos numéricos y el operador & (concatenación de cadenas) requiere argumentos de cadena. Si el argumento no puede convertirse al tipo de datos requerido, se sugiere un valor predeterminado. El valor predeterminado es el equivalente del valor nulo en el tipo correspondiente: cero para números, FALSE para valores booleanos, "" para cadenas, etc.
  
En la tabla siguiente se muestran ejemplos de expresiones y su resultado.
  
|**Expression**|**Resultado**|**Descripción**|
|:-----|:-----|:-----|
| 2 \* 5 &amp; " céntimos"  <br/> | "10 céntimos"  <br/> | El operador (concatenación de cadenas) requiere argumentos de cadena, por lo que el resultado numérico de 2 5 se convierte automáticamente en la cadena &amp; \* "10".  <br/> |
| 5 \* "2"  <br/> | 10    <br/> | El operador (multiplicación) requiere argumentos numéricos, por lo que la cadena "2" se convierte automáticamente al \* número equivalente 2.  <br/> |
| 5 \* "resalte"  <br/> | 0  <br/> | El operador (multiplicación) requiere argumentos numéricos, por lo que dado que la cadena "descarada" no se puede convertir en un número, se usa cero como \* su equivalente numérico.  <br/> |
   
## <a name="arithmetic-operators"></a>Operadores aritméticos

Los operadores aritméticos realizan operaciones con números. Los operadores más (+) y menos (-) pueden utilizarse solos como operadores unarios para indicar el signo de un número. El operador porcentaje (%) también es unario e identifica al número como un porcentaje.
  
|**Operador**|**Acción**|**Ejemplo**|**Resultado**|
|:-----|:-----|:-----|:-----|
| +  <br/> | Más unario  <br/> | +37  <br/> | 37  <br/> |
| -  <br/> | Menos unario  <br/> | -37  <br/> | -37  <br/> |
| %  <br/> | Porcentaje unario  <br/> | 37%  <br/> | .37  <br/> |
| ^  <br/> | Exponenciación  <br/> | 5 ^ 2  <br/> | 25  <br/> |
| \*  <br/> | Multiplicación  <br/> | 5 \* 2  <br/> | 10    <br/> |
| /  <br/> | División  <br/> | 5/2  <br/> | 2,5  <br/> |
| +  <br/> | Adición  <br/> | 5 +2  <br/> | 7   <br/> |
| -  <br/> | Sustracción  <br/> | 5 -2  <br/> | 3   <br/> |
   
## <a name="comparison-operators"></a>Operadores de comparación

Los operadores de comparación se utilizan para crear expresiones lógicas. Una expresión lógica da como resultado TRUE o FALSE.
  
|**Operador**|**Alternativa**|**Acción**|**Ejemplo**|**Resultado**|
|:-----|:-----|:-----|:-----|:-----|
| \>  <br/> | _GT_  <br/> | Mayor que  <br/> | 5 \> 2  <br/> | TRUE  <br/> |
| \<  <br/> | _LT_  <br/> | Menor que  <br/> | 5 \< 2  <br/> | FALSE  <br/> |
| \>=  <br/> | _GE_  <br/> | Mayor o igual que  <br/> | 5 \> = 2  <br/> | TRUE  <br/> |
| \<=  <br/> | _LE_  <br/> | Menor o igual que  <br/> | 5 \< = 2  <br/> | FALSE  <br/> |
| =  <br/> | _EQ_  <br/> | Igual a  <br/> | 5 = 2  <br/> | FALSE  <br/> |
| \<\>  <br/> | _NE_  <br/> | Distinto de  <br/> | 5 \< \> 2  <br/> | TRUE  <br/> |
   
Los operadores de comparación simbólicos ( \> \< , etc.) son la mejor opción para la mayoría de las comparaciones. Los operadores alternativos _(GT,_ _LT,_ etc.) realizan una comparación exacta con los 15 dígitos completos de precisión que Visio usa para almacenar valores internamente.
  
Al comparar valores redondeados o calculados con los operadores alternativos, es posible que el resultado sea FALSE cuando, en prácticamente todos los casos, debiera ser TRUE.
  
Al utilizar operadores de comparación para comparar cadenas de texto, éstas se convierten primero en valores numéricos. A las cadenas de texto que no pueden convertirse se les da el valor 0; por tanto, las comparaciones varían y pueden no producir el resultado esperado. Para hacer una comparación de cadenas estándar, utilice la función STRSAME o STRSAMEEX.
  
## <a name="order-of-evaluation"></a>Orden de evaluación

Cuando una fórmula contiene más de una expresión, el orden en que se evalúan las expresiones depende de la operación que se esté realizando. En la tabla siguiente se muestra el orden de evaluación de los operadores en Visio.
  
|**Order**|**Acción**|**Operador**|
|:-----|:-----|:-----|
|Primero  <br/> |Positivo  <br/> |+ (unario)  <br/> |
||Negativo  <br/> |- (unario)  <br/> |
||Porcentaje  <br/> |% (unario)  <br/> |
|Segundo  <br/> |Exponenciación  <br/> |^  <br/> |
|Tercera  <br/> |Multiplicación  <br/> |\*  <br/> |
||División  <br/> |/  <br/> |
|Cuarta  <br/> |Adición  <br/> |+  <br/> |
||Sustracción  <br/> |-  <br/> |
|Quinto  <br/> |Concatenación de cadenas  <br/> |&amp;  <br/> |
|Sexto  <br/> |Mayor que  <br/> |\> o GT  <br/> |
||Mayor o igual que  <br/> |\>= o GE  <br/> |
||Menor que  <br/> |\< o LT  <br/> |
||Menor o igual que  <br/> |\<= o LE  <br/> |
|Séptimo  <br/> |Igual  <br/> |= o EQ  <br/> |
||Distinto de  <br/> |\<\> o NE  <br/> |
   
Puede cambiar el orden de evaluación si encierra las expresiones entre paréntesis. Visio evalúa primero las expresiones entre paréntesis, de izquierda a derecha. Por ejemplo:
  
4 + 5 \* 6 = 4 + 30 = 34
  
(4 + 5) \* 6 = 9 \* 6 = 54
  
Si hay expresiones anidadas entre paréntesis, se evaluarán primero aquéllas de los paréntesis más internos.
  
## <a name="ampersand-operator"></a>Operador &

El operador & devuelve una nueva cadena de caracteres. Con este operador, puede crear palabras y frases compuestas. Utilice la sintaxis siguiente:
  
"string1" &amp; "string2"
  
 **Ejemplo**
  
"dog" &amp; "house" devuelve "doghouse"
  

