---
title: Propiedad Field. ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1ef68db39b7dcad380eae16f789f4dd5b0eab75f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292947"
---
# <a name="fieldvalidationrule-property-dao"></a>Propiedad Field. ValidationRule (DAO)


**Se aplica a:** Access 2013, Office 2013

Establece o devuelve un valor que valida los datos en un campo mientras se modifica o se agrega a una tabla (sólo para áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . ValidationRule

*expresión* Expresión que devuelve un objeto **Field** .

## <a name="remarks"></a>Comentarios

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
<td><p><strong>Índice</strong></p></td>
<td><p>No admitido</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
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
> Si establece la propiedad en una cadena concatenada con un valor que no sea entero, y los parámetros del sistema especifican un carácter no-. S decimal como una coma (por ejemplo, strRule = "Price &gt; " &amp; lngPrice e lngPrice = 125, 50), se producirá un error cuando el código intenta validar los datos. Esto se debe a que durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado del sistema y el motor SQL de base de datos Microsoft Access sólo acepta el carácter decimal estándar de Estados Unidos.


