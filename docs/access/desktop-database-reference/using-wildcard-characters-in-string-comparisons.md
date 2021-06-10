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
<td><p>* o %</p></td>
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


Puede usar un grupo de uno o varios caracteres (*charlist*) entre corchetes ( ) para coincidir con cualquier carácter individual de la expresión, y charlist puede incluir casi cualquier carácter en el conjunto de caracteres ANSI, incluidos los \[ \] dígitos.   Puede usar el corchete de apertura de caracteres especiales ( ), signo de interrogación (?), signo de número ( ) y asterisco ( ) para que coincidan directamente solo si están entre \[ \# \* corchetes. No puede usar el corchete de cierre ( ) dentro de un grupo para que coincida con sí mismo, pero puede usarlo fuera de un \] grupo como un carácter individual.

Además de una lista simple de caracteres incluidos entre corchetes, *listaDeCaracteres* puede especificar un intervalo de caracteres utilizando un guión (-) para separar los límites inicial y final del intervalo. Por ejemplo, el uso de A-Z en el patrón da como resultado una coincidencia si la posición de carácter correspondiente en la expresión contiene alguna de las letras mayúsculas del intervalo \[ \] A a Z.   Puede incluir varios intervalos entre corchetes sin delimitar los intervalos. Por ejemplo, \[ a-zA-Z0-9 \] coincide con cualquier carácter alfanumérico.

Es importante tener en cuenta que ansi SQL caracteres comodín (%) and ( \_ ) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet. Se tratarán como literales si se usan en Microsoft Access o DAO.

Otras reglas importantes de la coincidencia de patrones son:

- Un signo de exclamación ( ) al principio de charlist significa que se realiza una coincidencia si se encuentra algún carácter excepto los de \! *charlist* en la *expresión*.  Si se usa fuera de los corchetes, el signo de exclamación se corresponde consigo mismo.

- Puede usar el guión (-) al principio (a continuación de un signo de exclamación si se utiliza) o al final de *listaDeCaracteres* en correspondencia consigo mismo. En cualquier otra posición, el guión identifica un intervalo de caracteres ANSI.

- Cuando se especifica un intervalo de caracteres, éstos deben aparecer en un criterio de ordenación ascendente (A-Z o 0-100). \[A-Z \] es un patrón válido, pero \[ Z-A \] no lo es.

- La secuencia de caracteres se omite; se considera una cadena de \[ \] longitud cero ("").

