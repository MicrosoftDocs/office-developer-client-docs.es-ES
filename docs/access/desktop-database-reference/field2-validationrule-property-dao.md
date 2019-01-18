---
title: Propiedad Field2.ValidationRule (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713194"
---
# <a name="field2validationrule-property-dao"></a>Propiedad Field2.ValidationRule (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que valida los datos de un campo cuando se cambia o agrega a una tabla (únicamente áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . ValidationRule

*expresión* Expresión que devuelve un objeto **Field2** .

## <a name="remarks"></a>Observaciones

Los valores de configuración o valores devueltos son un String que describe una comparación en la forma de una cláusula SQL WHERE sin la palabra reservada WHERE. Para un objeto que todavía no está anexado a la colección **[Fields](fields-collection-dao.md)**, esta propiedad es de lectura y escritura.

La propiedad **ValidationRule** determina si un campo contiene o no datos válidos. Si los datos no son válidos, se produce un error capturable en tiempo de ejecución. El mensaje de error que se devuelve es el texto de la propiedad **ValidationText**, si se ha especificado, o el texto de la expresión especificada en **ValidationRule**.

Para un objeto **Field2**, la utilización de la propiedad **ValidationRule** depende del objeto que contiene la colección **Fields** a la que está anexado el objeto **Field2**.

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

La expresión de cadena que especifica la propiedad **ValidationRule** de un objeto **Field2** puede referirse sólo a ese **Field2**. Puede que la expresión no se refiera a las funciones definidas por el usuario, funciones agregadas de SQL o consultas. Para establecer un objeto **Field2** de la propiedad **ValidationRule** cuando el valor de la propiedad **ValidateOnSet** es **True**, la expresión se debe analizar correctamente (con el nombre del campo como un operando implícito) y se debe evaluar como **True**. Si el valor de la propiedad **ValidateOnSet** es **False**, el valor de la propiedad **ValidationRule** se omite.


> [!NOTE]
> Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strRule = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando el código intenta validar los datos. Esto se debe a que, durante la concatenación, el número se convertirá en una cadena que utiliza el carácter decimal predeterminado del sistema, y el motor de base de datos de Microsoft Access SQL sólo acepta caracteres decimales anglosajones.


