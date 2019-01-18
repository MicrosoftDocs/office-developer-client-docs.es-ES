---
title: Soporte del proveedor para ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703513"
---
# <a name="provider-support-for-adox"></a>Soporte del proveedor para ADOX


**Se aplica a**: Access 2013, Office 2013

Algunas características de ADOX no son compatibles; depende de cuál sea su proveedor de datos de OLE DB. ADOX es totalmente compatible con [Proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). A continuación, se indican las características no compatibles con [Proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md), [Proveedor de Microsoft OLE DB para ODBC](microsoft-ole-db-provider-for-odbc.md) o [Proveedor de Microsoft OLE DB para Oracle](microsoft-ole-db-provider-for-oracle.md). ADOX no es compatible con ningún otro proveedor de Microsoft OLE DB.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Proveedor de Microsoft OLE DB para SQL Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto o colección</p></th>
<th><p>Restricción de uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Catalog</strong></p></td>
<td><p>El método <strong>Create</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Tables</strong></p></td>
<td><p>Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Views</strong></p></td>
<td><p><strong>Views</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Procedures</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>Procedure</strong></p></td>
<td><p>La propiedad <strong>Comando</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Keys</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Users</strong></p></td>
<td><p><strong>Users</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Groups</strong></p></td>
<td><p><strong>Groups</strong> no es compatible.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a>Proveedor de Microsoft OLE DB para ODBC

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto o colección</p></th>
<th><p>Restricción de uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Catalog</strong></p></td>
<td><p>El método <strong>Create</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Tables</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.
 Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Procedures</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>Procedure</strong></p></td>
<td><p>La propiedad <strong>Comando</strong> no es compatible.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Indexes</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Keys</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Users</strong></p></td>
<td><p><strong>Users</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Groups</strong></p></td>
<td><p><strong>Groups</strong> no es compatible.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a>Proveedor de Microsoft OLE DB para Oracle

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto o colección</p></th>
<th><p>Restricción de uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Catalog</strong></p></td>
<td><p>El método <strong>Create</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Tables</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.
 Las propiedades son de lectura y escritura antes de la creación de objetos y de sólo lectura cuando hacen referencia a un objeto existente.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Views</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>View</strong></p></td>
<td><p>La propiedad <strong>Comando</strong> no es compatible.</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>Procedures</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>Procedure</strong></p></td>
<td><p>La propiedad <strong>Comando</strong> no es compatible.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Indexes</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Keys</strong></p></td>
<td><p>Los métodos <strong>Append</strong> y <strong>Delete</strong> no son compatibles.</p></td>
</tr>
<tr class="odd">
<td><p>Colección <strong>Users</strong></p></td>
<td><p><strong>Users</strong> no es compatible.</p></td>
</tr>
<tr class="even">
<td><p>Colección <strong>Groups</strong></p></td>
<td><p><strong>Groups</strong> no es compatible.</p></td>
</tr>
</tbody>
</table>

