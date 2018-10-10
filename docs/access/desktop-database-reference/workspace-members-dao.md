---
title: Workspace Members (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04dd82fcdb3bd9be0581ea5172429960769b31af
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486614"
---
# <a name="workspace-members-dao"></a>Workspace Members (DAO)


**Se aplica a**: Access 2013 | Office 2013

Un objeto Workspace define una sesión con nombre para un usuario. Contiene bases de datos abiertas y proporciona mecanismos para transacciones simultáneas y, en áreas de trabajo de Microsoft Access, compatibilidad con grupos de trabajo seguros.

## <a name="methods"></a>Métodos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Comienza una nueva transacción <strong>Database</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-close-method-dao.md">Cerrar</a></strong></p></td>
<td><p>Cierra un objeto <strong>Workspace</strong> abierto.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Finaliza la transacción actual y guarda los cambios.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="database-object-dao.md">Database</a></strong>, guarda la base de datos en el disco y devuelve un objeto <strong>Database</strong> abierto (sólo áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Abre un objeto <strong><a href="connection-object-dao.md">Connection</a></strong> en un origen de datos ODBC (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Abre una base de datos determinada en un objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> y devuelve una referencia al objeto <strong><a href="database-object-dao.md">Database</a></strong> que lo representa.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></p></td>
<td><p>Finaliza la transacción actual y restaura las bases de datos en el objeto <strong>Workspace</strong> en el estado en el que estaban cuando comenzó la transacción actual.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propiedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></p></td>
<td><p>Devuelve una colección <strong>Connections</strong> que representa las conexiones actuales del objeto <strong>Workspace</strong> especificado. Es de solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></p></td>
<td><p>Devuelve una colección <strong>Databases</strong> que representa las bases de datos abiertas del objeto <strong>Workspace</strong> especificado. Es de solo lectura</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</P>


<p>Establece o devuelve el tipo de controlador de cursor utilizado en la conexión creada por los métodos <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> o <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica si varias transacciones que implican los mismos motores de base de datos de Microsoft Access conectados al origen de datos ODBC están aisladas (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-name-property-dao.md">Name</a></strong></p></td>
<td><p>Devuelve o establece el nombre del objeto especificado. <strong>String</strong> de lectura y escritura si el objeto no se anexó a una colección. <strong>String</strong> de solo lectura si el objeto se anexó a una colección.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-properties-property-dao.md">Propiedades</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica el tipo operativo o el tipo de datos de un objeto. <strong>Integer</strong> de sólo lectura.</p></td>
</tr>
</tbody>
</table>

