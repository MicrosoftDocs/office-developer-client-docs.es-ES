---
title: Método Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ca2ccb4183a59c2b579fd4375f26aa4fd539532f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302586"
---
# <a name="workspaceopendatabase-method-dao"></a>Método Workspace.OpenDatabase (DAO)

**Se aplica a:** Access 2013, Office 2013

Abre una base de datos determinada en un objeto **[Workspace](workspace-object-dao.md)** y devuelve una referencia al objeto **[Database](database-object-dao.md)** que lo representa.

## <a name="syntax"></a>Sintaxis

*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*expression* Variable que representa un objeto **Workspace**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatorio</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Nombre de un archivo de base de datos del motor de base de datos de Microsoft Access existente o nombre de origen de datos (DSN) de un origen de datos ODBC. Vea la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más información sobre cómo establecer este valor.</p></td>
</tr>
<tr class="even">
<td><p><em>Opciones</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Establece varias opciones para la base de datos, tal como se especifica en Comentarios.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>True</strong> si quiere abrir la base de datos con un acceso de solo lectura o <strong>False</strong> (opción predeterminada) si quiere abrir la base de datos con un acceso de escritura/lectura.</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Especifica diversa información de conexión, incluidas las contraseñas.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor devuelto

Base de datos

## <a name="remarks"></a>Comentarios

Puede utilizar los valores siguientes para el argumento options.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>True</strong></p></td>
<td><p>Abre la base de datos en modo exclusivo.</p></td>
</tr>
<tr class="even">
<td><p><strong>False</strong></p></td>
<td><p>(Opción predeterminada) Abre la base de datos en modo compartido.</p></td>
</tr>
</tbody>
</table>

<br/>

Al abrir una base de datos, se agrega automáticamente a la colección **Databases**.

Al usar dbname, debe tener en cuenta ciertos aspectos:

- Si hace referencia a una base de datos que ya está abierta para que acceda otro usuario, se producirá un error.

- Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.

- Si es una cadena de longitud cero ("") y *connect* es "ODBC;", se mostrará un cuadro de diálogo con una lista de todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.

Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.

> [!NOTE]
> Al acceder al origen de datos ODBC conectado por el motor de base de datos de Microsoft Access, puede mejorar el rendimiento de su aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular objetos **[TableDef](tabledef-object-dao.md)** individuales a tablas específicas en el origen de datos ODBC.

## <a name="example"></a>Ejemplo

En este ejemplo se usa el método **OpenDatabase** para abrir una base de datos de Microsoft Access y dos bases de datos ODBC conectadas por el motor de base de datos de Microsoft Access.

```vb 
Sub OpenDatabaseX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsPubs As Database 
 Dim dbsPubs2 As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 ' Create Microsoft Access Workspace object. 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 
 ' Open Database object from saved Microsoft Access database 
 ' for exclusive use. 
 MsgBox "Opening Northwind..." 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb", _ 
 True) 
 
 ' Open read-only Database object based on information in 
 ' the connect string. 
 MsgBox "Opening pubs..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set dbsPubs = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverNoPrompt, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Database object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening second copy of pubs..." 
 Set dbsPubs2 = wrkAcc.OpenDatabase("Publishers", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 Debug.Print "Database properties for " & _ 
 dbsLoop.Name & ":" 
 
 On Error Resume Next 
 ' Enumerate the Properties collection of each Database 
 ' object. 
 For Each prpLoop In dbsLoop.Properties 
 If prpLoop.Name = "Connection" Then 
 ' Property actually returns a Connection object. 
 Debug.Print " Connection[.Name] = " & _ 
 dbsLoop.Connection.Name 
 Else 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 End If 
 Next prpLoop 
 On Error GoTo 0 
 
 Next dbsLoop 
 
 dbsNorthwind.Close 
 dbsPubs.Close 
 dbsPubs2.Close 
 wrkAcc.Close 
 
End Sub 
 
```

