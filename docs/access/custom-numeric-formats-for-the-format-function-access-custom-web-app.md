---
title: Formatos numéricos personalizados para la función Format (aplicación web personalizada de Access)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 97efe972-d873-47d7-be81-8ae3461870c4
description: Aprenda a controlar cómo se muestra un número mediante la creación de un formato numérico definido por el usuario.
ms.openlocfilehash: fac128ce13edf89105fbee7319533e1a3f346d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815355"
---
# <a name="custom-numeric-formats-for-the-format-function-access-custom-web-app"></a>Formatos numéricos personalizados para la función Format (aplicación web personalizada de Access)

Aprenda a controlar cómo se muestra un número mediante la creación de un formato numérico definido por el usuario.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/es-ES/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 

Puede cambiar el modo en que se muestra un número creando un formato de número definido por el usuario. Un formato de número definido por el usuario puede tener de una a tres secciones separadas por punto y coma (;). Si el argumento de estilo de la función [Función Format (aplicación web personalizada de Access)](format-function-access-custom-web-app.md) contiene uno de los formatos numéricos predefinidos, solo se permite una sección. 
  
## <a name="format-specifications"></a>Especificaciones de formato
<a name="bk_addresources"> </a>

En la siguiente tabla se muestran los caracteres que puede usar para crear formatos de números definidos por el usuario:
  
|**Especificación de formato**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Muestra el número sin formato.  <br/> |
|**0** (el carácter cero)  <br/> |Marcador de posición de dígitos. Muestra un dígito o un cero. Si la expresión tiene un dígito en la posición donde aparece el cero en la cadena de formato, muestra el dígito; de lo contrario, muestra un cero en esa posición.  <br/> Si el número tiene menos dígitos que ceros (en cualquier lado del decimal) en la expresión de formato, muestra ceros iniciales o finales. Si el número tiene más dígitos a la derecha del separador decimal que ceros a la derecha del separador decimal en la expresión de formato, redondea los número a tantos decimales como ceros haya. Si el número tiene más dígitos a la izquierda del separador decimal que ceros hay a la izquierda del separador decimal en la expresión de formato, muestra los dígitos adicionales sin modificación.  <br/> |
|#  <br/> |Marcador de posición de dígitos. Muestra un dígito o nada. Si la expresión tiene un dígito en la posición donde aparece el carácter # en la cadena de formato, muestra el dígito; de lo contrario, no muestra nada en esa posición.  <br/> Este símbolo funciona exactamente como un marcador de posición de dígito 0, excepto en que los ceros iniciales y finales no se muestran si el número tiene menos dígitos que caracteres #  hay en el lado del separador decimal en la expresión de formato.  <br/> |
|. (carácter de punto)  <br/> |Marcador de posición decimal. El marcador de posición decimal determina cuántos dígitos se muestran a la izquierda y a la derecha del separador decimal. Si la expresión de formato solo contiene caracteres # a la izquierda de este símbolo; los números menores que 1 comienzan con un separador decimal. Para mostrar un cero inicial con números fraccionarios, use el cero como el primer marcador de posición de dígitos a la izquierda del separador decimal. En algunas configuraciones regionales se usa una coma como separador decimal. El carácter real que se usa como un marcador de posición decimal en la salida con formato depende del formato de número reconocido por el sistema. Por lo tanto, debe usar el punto como marcador de posición decimal en los formatos incluso si están en una configuración regional que usa una coma como separador decimal. La cadena con formato aparecerá en el formato correcto para la configuración regional.  <br/> |
|%  <br/> |Marcador de posición de porcentaje. Multiplica la expresión por 100. El carácter de porcentaje (%) se inserta en la posición en la que aparece en la cadena de formato.  <br/> |
|, (carácter de coma)  <br/> |Separador de miles. El separador de miles separa los millares de las centenas en un número que tiene cuatro o más posiciones a la izquierda del separador decimal. El uso estándar del separador de miles se especifica si el formato contiene un separador de miles incluidos en los marcadores de posición de dígito (0 o #).  <br/> Un separador de miles inmediatamente a la izquierda del separador decimal (si se especifica un decimal) o como el caracter a la derecha de la cadena significa "escalar el número dividiéndolo por 1.000, redondeándolo según sea necesario". Los números menores que 1.000, pero mayores o iguales a 500, se muestran como 1 y los números menores que 500 se muestran como 0. Dos separadores de miles adyacentes en esta posición escalan por un factor de 1 millón y un factor adicional de 1.000 por cada separador adicional.  <br/> Varios separadores en cualquier posición que no sea inmediatamente a la izquierda del separador decimal o la posición más a la derecha de la cadena, solo se consideran que especifican el uso de un separador de miles. En algunas configuraciones regionales, se usa un punto como separador de miles. El carácter real que se usa como separador de miles en la salida con formato depende del formato de número reconocido por el sistema. Por lo tanto, debe usar la coma como separador de miles en los formatos, incluso si están en una configuración regional que usa un punto como separador de miles. La cadena con formato aparecerá en el formato correcto de la configuración regional.  <br/> Por ejemplo, considere las siguientes tres cadenas de formato:  <br/> "#, 0.", que usa el separador de miles para dar formato al número 100 millones como la cadena "100,000,000".  <br/> "#0,.", que usa una escala por un factor de mil para dar formato al número 100 millones como la cadena "100000".  <br/> "#, 0,.", que usa el separador de miles y escala por mil para dar formato al número 100 millones como la cadena "100,000".  <br/> |
|: (carácter de dos puntos)  <br/> |Separador de hora. En algunas configuraciones regionales, se pueden usar otros caracteres para representar el separador de hora. El separador de hora separa las horas, los minutos y los segundos cuando los valores de hora tienen formato. El carácter real que se usa como separador de hora en las salida con formato se determina por la configuración del sistema.  <br/> |
|/ (carácter de barra diagonal)  <br/> |Separador de fecha. En algunas configuraciones regionales, se pueden usar otros caracteres para representar el separador de fecha. El separador de fecha separa el día, el mes y el año cuando los valores de fecha tienen formato. El carácter real que se usa como separador de fecha en la salida con formato se determina por la configuración del sistema.  <br/> |
|**E- , E+ , e- , e+** <br/> |Formato científico. Si la expresión de formato contiene al menos un marcador de posición de dígito (0 o #) a la izquierda de E-, E+, e- o e+, se muestra el número en formato científico y E o e se inserta entre el número y su exponente. El número de marcadores de posición de dígitos a la izquierda determina el número de dígitos del exponente. Use E- o e- para colocar un signo menos junto a los exponentes negativos. Use E+ o e+ para colocar un signo menos junto a los exponentes negativos y un signo más junto a los exponentes positivos. También debe incluir marcadores de posición de dígitos a la derecha de este símbolo para lograr un formato correcto.  <br/> |
|**- + $ ( )** <br/> |Caracteres literales. Estos caracteres se muestran exactamente como se escriben en la cadena de formato. Para mostrar un carácter distinto de los enumerados, preceda una barra diagonal inversa (\) o enciérrelo entre comillas dobles ("").  <br/> |
|\ (barra diagonal inversa)  <br/> |Muestra el siguiente carácter en la cadena de formato. Para mostrar un carácter que tenga un significado especial, como un carácter literal, preceda una barra diagonal inversa (\). La barra diagonal inversa no se muestra. Usar una barra diagonal inversa es lo mismo que incluir el siguiente carácter entre comillas dobles. Para mostrar una barra diagonal inversa, use dos barras diagonales inversas (\\).  <br/> Ejemplos de caracteres que no se pueden mostrar como caracteres literales son los caracteres de formato de fecha y de hora (a, c, d, h, m, n, p, q, s, t, w, y, / y :), los caracteres de formato numérico (#, 0, %, E, e, coma y punto) y los caracteres de formato de cadena (@, &amp;, \<, \> y !).  <br/> |
|"ABC"  <br/> |Muestra la cadena entre comillas dobles (""). Para incluir una cadena en el argumento de estilo desde el código, debe usar Chr(34) para encerrar el texto (34 es el código de carácter para las comillas (")).  <br/> |
   
La siguiente tabla contiene algunos ejemplos de expresiones de formato para números. (Estos ejemplos asumen que los ajustes de configuración regional del sistema es inglés de Estados Unidos) La primera columna contiene las cadenas de formato para la función Format. Las demás columnas contienen la salida resultante si los datos con formato tienen el valor dado en los encabezados de columna.
  
|**Formato (estilo)**|**"5" con formato como**|**"-5" con formato como**|**"0.5" con formato como**|**"0" con formato como**|
|:-----|:-----|:-----|:-----|:-----|
|Cadena de longitud cero ("")  <br/> |5  <br/> |-5  <br/> |0.5  <br/> |0  <br/> |
|0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|0.00  <br/> |5.00  <br/> |-5.00  <br/> |0.50  <br/> |0.00  <br/> |
|#,##0  <br/> |5  <br/> |-5  <br/> |1  <br/> |0  <br/> |
|$#,##0;($#,##0)  <br/> |$5  <br/> |($5)  <br/> |$1  <br/> |$0  <br/> |
|$#,##0.00;($#,##0.00)  <br/> |$5.00  <br/> |($5.00)  <br/> |$0.50  <br/> |$0.00  <br/> |
|0%  <br/> |500%  <br/> |-500%  <br/> |50%  <br/> |0%  <br/> |
|0.00%  <br/> |500.00%  <br/> |-500.00%  <br/> |50.00%  <br/> |0.00%  <br/> |
|0.00E+00  <br/> |5.00E+00  <br/> |-5.00E+00  <br/> |5.00E-01  <br/> |0.00E+00  <br/> |
|0.00E-00  <br/> |5.00E00  <br/> |-5.00E00  <br/> |5.00E-01  <br/> |0.00E00  <br/> |
|"$#,##0;;\Z\e\r\o"  <br/> |$5  <br/> |$-5  <br/> |$1  <br/> |Zero  <br/> |
   
## <a name="remarks"></a>Comentarios
<a name="bk_addresources"> </a>

Si incluye puntos y coma sin nada entre ellos, la sección faltante se muestra con el formato del valor positivo.
  
## <a name="see-also"></a>Vea también

- [Función Format (aplicación web personalizada de Access)](format-function-access-custom-web-app.md) 
- [Formatos de fecha y hora personalizados para la función Format (aplicación web personalizada de Access)](custom-date-and-time-formats-for-the-format-function-access-custom-web-app.md)
  

