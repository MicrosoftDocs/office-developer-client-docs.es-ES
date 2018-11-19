---
title: Uso de caracteres comodín en comparaciones de cadenas
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fb6c63d5d2db1db54d52a03fef41e44a29f42c9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026171"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>Uso de caracteres comodín en comparaciones de cadenas

**Se aplica a**: Access 2013, Office 2013

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
<td><p>*o %</p></td>
<td><p>Cero o más caracteres</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Un único dígito (0 – 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>listaDeCaracteres</em>]</p></td>
<td><p>Cualquier carácter de <em>listaDeCaracteres</em></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>listaDeCaracteres</em>]</p></td>
<td><p>Cualquier carácter no incluido en <em>listaDeCaracteres</em></p></td>
</tr>
</tbody>
</table>


Puede utilizar un grupo de uno o varios caracteres (*listacaracteres*) entre corchetes (\[ \]) para que coincida con cualquier carácter único en *expresión* y *listacaracteres* puede incluir casi cualquier carácter en el carácter ANSI establecidas, incluyendo dígitos. Puede usar los caracteres especiales corchete de apertura (\[ ), el signo de interrogación (?), signo de número (\#) y el asterisco (\*) para que coincida con ellos mismos directamente sólo si están entre corchetes. No se puede usar el corchete de cierre ( \]) dentro de un grupo para que coincida con sí mismo, pero se puede usar fuera de un grupo como un carácter individual.

Además de una lista simple de caracteres incluidos entre corchetes, *listacaracteres* puede especificar un intervalo de caracteres mediante un guión (-) para separar la parte superior y los límites inferiores del rango. Por ejemplo, mediante \[A Z\] en *modelo* da como resultado una coincidencia si la posición del carácter correspondiente en *expresión* contiene cualquiera de las letras mayúsculas en el intervalo de la a la Z. Puede incluir varios intervalos dentro de los corchetes sin delimitar los intervalos. Por ejemplo, \[a-zA-Z0-9\] coincide con cualquier carácter alfanumérico.

Es importante tener en cuenta que los caracteres comodín de ANSI SQL (%) y (\_) sólo están disponibles con Microsoft Jet versión 4.X y el proveedor Microsoft OLE DB para Jet. Se tratarán como literales si se usan en Microsoft Access o DAO.

Otras reglas importantes de la coincidencia de patrones son:

- Un signo de exclamación (\!) al principio de *listacaracteres* significa que se realiza una coincidencia si cualquier carácter excepto incluido en *listaDeCaracteres* se encuentra en la *expresión*. Si se usa fuera de los corchetes, el signo de exclamación se corresponde consigo mismo.

- Puede usar el guión (-) al principio (después de un signo de exclamación si se utiliza uno) o al final de *listacaracteres* para que coincida con el propio. En cualquier otra posición, el guión identifica un intervalo de caracteres ANSI.

- Cuando se especifica un intervalo de caracteres, éstos deben aparecer en un criterio de ordenación ascendente (A-Z o 0-100). \[A-z\] es un patrón válido, pero \[Z-A\] no es.

- La secuencia de caracteres \[ \] se omite; se considera una cadena de longitud cero ("").

