---
title: Proveedor de Microsoft OLE DB para Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e473176ae6a34d04fc316a8d5075e414f6c8e98
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868150"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a>Proveedor de Microsoft OLE DB para Oracle

**Se aplica a**: Access 2013, Office 2013

El Proveedor de Microsoft OLE DB para Oracle permite que ADO obtenga acceso a bases de datos de Oracle.

## <a name="connection-string-parameters"></a>Parámetros de la cadena de conexión

Para conectar con este proveedor, establezca el argumento *Provider* de la propiedad [ConnectionString](connectionstring-property-ado.md) en:

```vb 
 
MSDAORA 
```

La lectura de la propiedad [Provider](provider-property-ado.md) devolverá también esta cadena.

Si se ejecuta una consulta conjunta con un conjunto de claves o cursor dinámico en una base de datos de Oracle, se produce un error. Oracle solamente admite un cursor estático de sólo lectura.

## <a name="typical-connection-string"></a>Cadena de conexión típica

Una típica cadena de conexión de este proveedor es:

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

La cadena consta de estas palabras clave:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Palabra clave</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Especifica el Proveedor OLE DB para Oracle.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Especifica el nombre de un servidor.</p></td>
</tr>
<tr class="odd">
<td><p><strong>User ID</strong></p></td>
<td><p>Especifica el nombre de usuario.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Especifica la contraseña de usuario.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Parámetros de conexión específicos del proveedor

El proveedor admite varios parámetros de conexión específicos del proveedor además de los definidos por ADO. Al igual que las propiedades de conexión ADO, estas propiedades específicas del proveedor se pueden establecer mediante la colección [Properties](properties-collection-ado.md) de un objeto [Connection](connection-object-ado.md) o como parte de **ConnectionString**.

Estos parámetros se describen en profundidad en la Referencia del programador de OLE DB. (El [Índice de propiedades dinámicas de ADO](ado-dynamic-property-index.md) proporciona una referencia cruzada entre estos nombres de parámetro y las propiedades de OLE DB correspondientes.)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Parámetro</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Window Handle</strong></p></td>
<td><p>Indica el controlador de ventana que se utilizará para solicitar información adicional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>Indica un número exclusivo de 32 bits (por ejemplo, 1033) que especifica las preferencias relacionadas con el idioma del usuario. Estas preferencias indican el formato de las fechas y las horas, el modo en que los elementos se ordenan alfabéticamente y en que se comparan las cadenas, etc.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OLE DB Services</strong></p></td>
<td><p>Indica una máscara de bits que especifica los servicios OLE DB que se van a habilitar o deshabilitar.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>Indica si es necesario preguntar al usuario mientras se está estableciendo una conexión.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Extended Properties</strong></p></td>
<td><p>Una cadena que contiene información de conexión ampliada específica del proveedor. Utilice esta propiedad únicamente para la información de conexión específica del proveedor que no se pueda describir por medio del mecanismo de la propiedad.</p></td>
</tr>
</tbody>
</table>

