---
title: Propiedad Field.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 977bdfa921ea99db82fd2a429fcfba53680140f3
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937256"
---
# <a name="fieldvalidationrule-property-dao"></a>Propiedad Field.ValidationRule (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que valida los datos de un campo cuando se cambia o agrega a una tabla (únicamente áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . ValidationRule

*expresión* Expresión que devuelve un objeto **Field** .

## <a name="remarks"></a>Observaciones

Los valores de configuración o los valores devueltos son un objeto String que describe una comparación en forma de una cláusula WHERE SQL sin la palabra reservada WHERE. Para un objeto no anexado todavía a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura.

La propiedad **ValidationRule** determina si un campo contiene o no datos válidos. Si los datos no son válidos, se produce un error en tiempo de ejecución capturable. El mensaje de error devuelto es el texto de la propiedad **[ValidationText](field-validationtext-property-dao.md)**, si se especifica, o el texto de la expresión especificada por **ValidationRule**.

Para un objeto **[Field](field-object-dao.md)**, el uso de la propiedad **ValidationRule** dependerá del objeto que contenga la colección **Fields** a la que se anexa el objeto **Field**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto anexado a</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p><strong>Objeto QueryDef</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Solo lectura</p></td>
</tr>
<tr class="even">
<td><p><strong>Relación</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lectura y escritura</p></td>
</tr>
</tbody>
</table>


La validación sólo se admite en las bases de datos que utilizan el motor de base de datos Microsoft Access.

La expresión de cadena especificada por la propiedad **ValidationRule** de un objeto **Field** puede referirse sólo a ese **Field**. Puede que la expresión no se refiera a las funciones definidas por el usuario, funciones agregadas de SQL o consultas. Para establecer un objeto **Field** de la propiedad **ValidationRule** cuando el valor de la propiedad **ValidateOnSet** es **True**, la expresión se debe analizar correctamente (con el nombre del campo como un operando implícito) y se debe evaluar a **True**. Si el valor de la propiedad **ValidateOnSet** es **False**, el valor de la propiedad **ValidationRule** se omite.


> [!NOTE]
> Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strRule = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando el código intenta validar los datos. Esto se debe a que, durante la concatenación, el número se convertirá en una cadena que utiliza el carácter decimal predeterminado del sistema, y el motor de base de datos de Microsoft Access SQL sólo acepta caracteres decimales anglosajones.


