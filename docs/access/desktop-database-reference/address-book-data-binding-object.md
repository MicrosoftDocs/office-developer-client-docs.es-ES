---
title: Objeto de enlace de datos de la Libreta de direcciones
TOCTitle: Address Book Data-Binding object
ms:assetid: cf43f645-1ee1-8655-eb70-86d601e9f3f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250030(v=office.15)
ms:contentKeyID: 48547807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fb5302d1c2b8e4eebb6dbe1a5906459834b8e41
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704304"
---
# <a name="address-book-data-binding-object"></a>Objeto de enlace de datos de la Libreta de direcciones


**Se aplica a**: Access 2013, Office 2013

La aplicación Libreta de direcciones utiliza el objeto [ RDS.DataControl ](datacontrol-object-rds.md) para enlazar datos de la base de datos de SQL Server a un objeto visual (en este caso, una tabla DHTML) en la página HTML cliente de la aplicación. La lógica del programa VBScript controlada por evento utiliza el objeto [RDS.DataControl](datacontrol-object-rds.md) para:

  - Consultar la base de datos, enviar actualizaciones a la base de datos y actualizar la cuadrícula de datos.

  - Permitir a los usuarios desplazarse al registro primero, siguiente, anterior o último en la cuadrícula de datos.

El código siguiente define el componente **RDS.DataControl**:

```vb 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
   ID=DC1 Width=1 Height=1> 
   <PARAM NAME="SERVER" VALUE="https://<%=Request.ServerVariables("SERVER_NAME")%>"> 
   <PARAM NAME="CONNECT" VALUE="Provider=sqloledb; 
Initial Catalog=AddrBookDb;Integrated Security=SSPI;"> 
</OBJECT> 
```

La etiqueta OBJECT define el componente **RDS.DataControl** en el programa. La etiqueta incluye dos tipos de parámetros:

  - Aquéllos asociados con la etiqueta genérica OBJECT.

  - Aquéllos específicos del objeto **RDS.DataControl**.

## <a name="generic-object-tag-parameters"></a>Parámetros genéricos de la etiqueta OBJECT

En la tabla siguiente, se describen los parámetros asociados con la etiqueta OBJECT.

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
<td><p><strong><em>CLASSID</em></strong></p></td>
<td><p>Un número único de 128 bits que identifica el tipo de objeto incrustado en el sistema. Este identificador se mantiene en el Registro del sistema del equipo local (para obtener más información de los identificadores de clase del objeto <strong>RDS.DataControl</strong>, vea <a href="datacontrol-object-rds.md">RDS.DataControl Object</a>).</p></td>
</tr>
<tr class="even">
<td><p><strong><em>ID</em></strong></p></td>
<td><p>Define un identificador del objeto incrustado (válido en todo un documento) que se utiliza para identificarlo en el código.</p></td>
</tr>
</tbody>
</table>


## <a name="rdsdatacontrol-tag-parameters"></a>Parámetros de etiqueta de RDS.DataControl

En la tabla siguiente, se describen los parámetros específicos del objeto **RDS.DataControl** (para obtener una lista completa de los parámetros del objeto **RDS.DataControl** y de cuándo implementarlos, vea [RDS.DataControl (objeto)](datacontrol-object-rds.md)).

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
<td><p><a href="server-property-rds.md">SERVIDOR</a></p></td>
<td><p>Si está utilizando HTTP, el valor es el nombre del equipo servidor precedido por https://.</p></td>
</tr>
<tr class="even">
<td><p><a href="connect-property-rds.md">CONECTAR</a></p></td>
<td><p>Proporciona la información de conexión necesaria para que el objeto <strong>RDS.DataControl</strong> se conecte al servidor SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado">SQL</a></p></td>
<td><p>Establece o devuelve la cadena de consulta usada para recuperar el objeto <a href="recordset-object-ado.md">Recordset</a>.</p></td>
</tr>
</tbody>
</table>

