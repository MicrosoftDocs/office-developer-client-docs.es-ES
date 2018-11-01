---
title: Recordset2.ValidationRule Property (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0c6df32c37f73dadf1df43201090d44d81a6a01
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890949"
---
# <a name="recordset2validationrule-property-dao"></a>Recordset2.ValidationRule Property (DAO)


**Se aplica a**: Access 2013, Office 2013

Establece o devuelve un valor que valida los datos en un campo mientras se modifica o se agrega a una tabla (sólo para áreas de trabajo de Microsoft Access). **String** de lectura y escritura.

## <a name="syntax"></a>Sintaxis

*expresión* . ValidationRule

*expresión* Variable que representa un objeto **Recordset2** .

## <a name="remarks"></a>Observaciones

La configuración o los valores devueltos son de tipo **String** que describe una comparación en el formulario de una cláusula SQL WHERE sin la palabra reservada WHERE. Para un objeto que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.

La propiedad **ValidationRule** determina si un campo contiene o no datos válidos. Si los datos no son válidos, se produce un error capturable en tiempo de ejecución. El mensaje de error que se devuelve es el texto de la propiedad **ValidationText**, si se ha especificado, o el texto de la expresión especificada en **ValidationRule**.

Para un objeto **Recordset**, el uso de la propiedad **ValidationRule** es de solo lectura. Para un objeto **TableDef**, el uso de la propiedad **ValidationRule** depende del estado del objeto **TableDef**, como se muestra en la siguiente tabla.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>TableDef</p></th>
<th><p>Uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Tabla base</p></td>
<td><p>Lectura y escritura</p></td>
</tr>
<tr class="even">
<td><p>Tabla vinculada</p></td>
<td><p>Sólo lectura</p></td>
</tr>
</tbody>
</table>


La validación sólo se admite en las bases de datos que utilizan el motor de base de datos Microsoft Access.

La expresión de cadena especificada por la propiedad **ValidationRule** de un objeto **Field** puede referirse sólo a ese **Field**. Puede que la expresión no se refiera a las funciones definidas por el usuario, funciones agregadas de SQL o consultas. Para establecer un objeto **Field** de la propiedad **ValidationRule** cuando el valor de la propiedad **ValidateOnSet** es **True**, la expresión se debe analizar correctamente (con el nombre del campo como un operando implícito) y se debe evaluar a **True**. Si el valor de la propiedad **ValidateOnSet** es **False**, el valor de la propiedad **ValidationRule** se omite.

La propiedad **ValidationRule** de un objeto **Recordset** o **TableDef** puede hacer referencia a varios campos en esos objetos. Se aplican las restricciones comentadas anteriormente en este tema para el objeto **Field**.

Para un objeto **Recordset** tipo Table, la propiedad **ValidationRule** hereda el valor de la propiedad **ValidationRule** del objeto **TableDef** que usa para crear un objeto **Recordset** tipo Table.


> [!NOTE]
> <P>Si se establece la propiedad en una cadena que se concatena con un valor no entero, y los parámetros del sistema especifican un carácter decimal que no sean-US como una coma (por ejemplo, strRule = "PRICE &gt; " &amp; lngPrice y lngPrice = 125,50), se producirá un error cuando el código intenta validar los datos. Esto se produce porque durante la concatenación, el número se convertirá en una cadena utilizando el carácter decimal predeterminado de su sistema y Microsoft Access SQL sólo acepta caracteres decimales con el formato estándar de Estados Unidos.</P>


