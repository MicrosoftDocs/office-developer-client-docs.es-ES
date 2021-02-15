---
title: Miembros DBEngine (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294284"
---
# <a name="dbengine-members-dao"></a>Miembros DBEngine (DAO)


**Se aplica a:** Access 2013, Office 2013

El objeto DBEngine es el objeto de nivel superior en el modelo de objetos DAO.

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
<td><p><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Inicia una nueva transacción. <strong>Database</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Termina la transacción actual y guarda los cambios.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></p></td>
<td><p>Copia y compacta una base de datos cerrada, y permite cambiar su versión, el orden de intercalación y el cifrado. (Solo áreas de trabajo de Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="database-object-dao.md">Database</a></strong>, guarda la base de datos en el disco y devuelve un objeto <strong>Database</strong> abierto (sólo áreas de trabajo de Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></p></td>
<td><p>Crea un nuevo objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-idle-method-dao.md">Inactivo</a></strong></p></td>
<td><p>Suspende el procesamiento de datos y habilita el motor de base de datos de Microsoft Access para que realice las tareas pendientes, como la optimización de memoria o los tiempos de espera de paginación (sólo en áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p>Uno de los <strong><a href="workspacetypeenum-enumeration-dao.md">valores workspaceTypeEnum.</a></strong></p>
<td><p><strong>NOTA</strong>: las áreas de trabajo de ODBCDirect no se admiten en Microsoft Access 2013. Use ADO si desea obtener acceso a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</p>
<p>Abre un objeto <strong><a href="connection-object-dao.md">Connection</a></strong> en un origen de datos ODBC (sólo áreas de trabajo de ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Abre una base de datos determinada y devuelve una referencia al objeto <strong><a href="database-object-dao.md">Database</a></strong> que lo representa.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></p></td>
<td><p>Proporciona información de conexión para un origen de datos ODBC en el Registro de Windows. El controlador ODBC necesita información de conexión cuando se abre el origen de datos ODBC durante una sesión.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-rollback-method-dao.md">Reversión</a></strong></p></td>
<td><p>Termina la transacción actual y restablece las bases de datos del objeto <strong>Workspace</strong> al estado que tenían antes de que comenzara la transacción actual.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></p></td>
<td><p>Anula temporalmente los valores para las claves del motor de base de datos de Microsoft Access en el Registro de Windows (sólo áreas de trabajo de Microsoft Access).</p></td>
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
<td><p><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></p></td>
<td><p>Establece la contraseña utilizada para crear el objeto <strong>Workspace</strong> predeterminado cuando se inicializa. <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></p></td>
<td><p>Establece o devuelve un valor que indica qué tipo de área de trabajo se utilizará en el siguiente objeto <strong><a href="workspace-object-dao.md">Workspace</a></strong> que se cree.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></p></td>
<td><p>Establece el nombre de usuario utilizado para crear el objeto <strong>Workspace</strong> predeterminado cuando se inicializa. <strong>String</strong> de lectura y escritura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-errors-property-dao.md">Errores</a></strong></p></td>
<td><p>Devuelve una colección <strong>Errors</strong> que contiene todos los objetos <strong>Error</strong> almacenados para el objeto especificado. Es de solo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></p></td>
<td><p>Establece o devuelve información sobre la clave del Registro de Windows que contiene los valores para el motor de base de datos Microsoft Access (sólo para áreas de trabajo de Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Establece o devuelve el número de segundos transcurridos antes de que se produzca un error cuando se intenta iniciar sesión en una base de datos ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Devuelve la colección <strong><a href="properties-collection-dao.md">Properties</a></strong> de un objeto especificado. Solo lectura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-version-property-dao.md">Versión</a></strong></p></td>
<td><p>Devuelve la versión de DAO que se está utilizando. <strong>String</strong> de sólo lectura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></p></td>
<td><p>Devuelve una colección <strong>Workspaces</strong> que contiene todos los objetos <strong>Workspace</strong> activos que no están ocultos. Solo lectura.</p></td>
</tr>
</tbody>
</table>

