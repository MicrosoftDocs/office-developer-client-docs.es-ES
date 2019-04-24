---
title: Uso de caracteres comodín en comparaciones de cadenas
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305939"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>Uso de caracteres comodín en comparaciones de cadenas

**Se aplica a:** Access 2013, Office 2013

La coincidencia de patrones integrada proporciona una herramienta versátil para realizar comparaciones de cadenas. En la siguiente tabla, se muestran los caracteres comodín que puede usar con el operador **Like** y el número de dígitos o cadenas con los que se corresponden.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Caracteres en <em>patrón</em></p></th>
<th><p>Correspondencia en <em>expresión</em></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? o _ (subrayado)</p></td>
<td><p>Cualquier carácter</p></td>
</tr>
<tr class="even">
<td><p>*o</p></td>
<td><p>Cero o más caracteres</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Un único dígito (0 – 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>charlist</em>]</p></td>
<td><p>Cualquier carácter de <em>listaDeCaracteres</em></p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p>Un único carácter no incluido en <em>listaDeCaracteres</em></p></td>
</tr>
</tbody>
</table>


Puede usar un grupo de uno o varios caracteres (*listacaracteres*) que se encuentran entre corchetes (\[ \]) para hacer coincidir cualquier carácter individual de la *expresión,* y *listacaracteres* puede incluir casi cualquier carácter del juego de caracteres ANSI, incluido dígitos. Puede usar los caracteres especiales corchete de\[ apertura (), signo de interrogación (?)\#, signo de almohadilla (\*) y asterisco () para que se ajusten a ellos mismos directamente sólo si están entre corchetes. No puede usar el corchete \]de cierre () dentro de un grupo para hacer coincidir consigo mismo, pero puede usarlo fuera de un grupo como un carácter individual.

Además de una lista simple de caracteres incluidos entre corchetes, *listaDeCaracteres* puede especificar un intervalo de caracteres utilizando un guión (-) para separar los límites inicial y final del intervalo. Por ejemplo, el \[uso de A\] -Z en un *patrón* da como resultado una coincidencia si la posición del carácter correspondiente en *expresión* contiene cualquiera de las letras mayúsculas en el rango de la a a la Z. Puede incluir varios intervalos dentro de los corchetes sin delimitar los intervalos. Por ejemplo, \[a-Za-z0-9\] coincide con cualquier carácter alfanumérico.

Es importante tener en cuenta que los caracteres comodín de ANSI SQL (%) y (\_) solo están disponibles con Microsoft Jet versión 4. X y el proveedor de Microsoft OLE DB para Jet. Se tratarán como literales si se usan en Microsoft Access o DAO.

Otras reglas importantes de la coincidencia de patrones son:

- Un signo de exclamación\!() al principio de *charlist* significa que se realiza una coincidencia si se encuentra en la *expresión*cualquier carácter excepto los que estén en *charlist* . Si se usa fuera de los corchetes, el signo de exclamación se corresponde consigo mismo.

- Puede usar el guión (-) al principio (a continuación de un signo de exclamación si se utiliza) o al final de *listaDeCaracteres* en correspondencia consigo mismo. En cualquier otra posición, el guión identifica un intervalo de caracteres ANSI.

- Cuando se especifica un intervalo de caracteres, éstos deben aparecer en un criterio de ordenación ascendente (A-Z o 0-100). \[A-Z\] es un patrón válido, pero \[Z-a\] no lo es.

- La secuencia \[ \] de caracteres no se tiene en cuenta; se considera una cadena de longitud cero ("").

