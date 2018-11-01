---
title: Método Workspace.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: dbb93908-ec3e-f3ee-c4ea-cca48340b4d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835343(v=office.15)
ms:contentKeyID: 48548108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd82a8159ae0a0f9388f62ff5db32e8d7989ef2e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883445"
---
# <a name="workspaceopendatabase-method-dao"></a><span data-ttu-id="08c1d-102">Método Workspace.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="08c1d-102">Workspace.OpenDatabase Method (DAO)</span></span>

<span data-ttu-id="08c1d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08c1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08c1d-104">Abre una base de datos determinada en un objeto **[Workspace](workspace-object-dao.md)** y devuelve una referencia al objeto **[Database](database-object-dao.md)** que lo representa.</span><span class="sxs-lookup"><span data-stu-id="08c1d-104">Opens a specified database in a **[Workspace](workspace-object-dao.md)** object and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08c1d-105">Syntax</span></span>

<span data-ttu-id="08c1d-106">*expresión* . OpenDatabase (***nombre***, ***Opciones***, ***ReadOnly***, ***Conectar***)</span><span class="sxs-lookup"><span data-stu-id="08c1d-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="08c1d-107">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="08c1d-107">*expression* A variable that represents a **Workspace** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="08c1d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08c1d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08c1d-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="08c1d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="08c1d-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="08c1d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="08c1d-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="08c1d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="08c1d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="08c1d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08c1d-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="08c1d-113">Name</span></span></p></td>
<td><p><span data-ttu-id="08c1d-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="08c1d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="08c1d-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="08c1d-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="08c1d-p101">Nombre de un archivo de base de datos del motor de base de datos de Microsoft Access existente o nombre de origen de datos (DSN) de un origen de datos ODBC. Vea la propiedad <strong><a href="connection-name-property-dao.md">Name</a></strong> para obtener más información sobre cómo establecer este valor.  </span><span class="sxs-lookup"><span data-stu-id="08c1d-p101">the name of an existing Microsoft Access database engine database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c1d-118">Options</span><span class="sxs-lookup"><span data-stu-id="08c1d-118">Options</span></span></p></td>
<td><p><span data-ttu-id="08c1d-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="08c1d-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="08c1d-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="08c1d-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="08c1d-121">Establece varias opciones para la base de datos, tal como se especifica en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="08c1d-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08c1d-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="08c1d-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="08c1d-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="08c1d-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="08c1d-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="08c1d-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="08c1d-125"><strong>True</strong> si quiere abrir la base de datos con un acceso de solo lectura o <strong>False</strong> (opción predeterminada) si quiere abrir la base de datos con un acceso de escritura/lectura.</span><span class="sxs-lookup"><span data-stu-id="08c1d-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c1d-126">Conexión</span><span class="sxs-lookup"><span data-stu-id="08c1d-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="08c1d-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="08c1d-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="08c1d-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="08c1d-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="08c1d-129">Especifica diversa información de conexión, incluidas las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="08c1d-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="08c1d-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08c1d-130">Return value</span></span>

<span data-ttu-id="08c1d-131">Base de datos</span><span class="sxs-lookup"><span data-stu-id="08c1d-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="08c1d-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="08c1d-132">Remarks</span></span>

<span data-ttu-id="08c1d-133">Puede utilizar los valores siguientes para el argumento options.</span><span class="sxs-lookup"><span data-stu-id="08c1d-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08c1d-134">Configuración</span><span class="sxs-lookup"><span data-stu-id="08c1d-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="08c1d-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="08c1d-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08c1d-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="08c1d-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="08c1d-137">Abre la base de datos en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="08c1d-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08c1d-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="08c1d-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="08c1d-139">(Opción predeterminada) Abre la base de datos en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="08c1d-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="08c1d-140">Al abrir una base de datos, se agrega automáticamente a la colección **Databases**.</span><span class="sxs-lookup"><span data-stu-id="08c1d-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="08c1d-141">Se aplican determinadas consideraciones cuando se utiliza dbname:</span><span class="sxs-lookup"><span data-stu-id="08c1d-141">Some considerations apply when you use dbname:</span></span>

- <span data-ttu-id="08c1d-142">Si se refiere a una base de datos que ya está abierta para que tenga acceso a ella otro usuario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="08c1d-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

- <span data-ttu-id="08c1d-143">Si no se refiere a una base de datos existente o a un nombre de origen de datos ODBC válido, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="08c1d-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

- <span data-ttu-id="08c1d-144">Si es una cadena de longitud cero ("") y *Conectar* es "ODBC;", se muestra un cuadro de diálogo lista de todos los nombres de orígenes de datos ODBC para el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="08c1d-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="08c1d-145">Para cerrar una base de datos y eliminar el objeto **Database** de la colección **Databases**, use el método **[Close](connection-close-method-dao.md)** del objeto.</span><span class="sxs-lookup"><span data-stu-id="08c1d-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>

> [!NOTE]
> <span data-ttu-id="08c1d-146">[!NOTA] Al acceder al origen de datos ODBC conectado por el motor de base de datos de Microsoft Access, puede mejorar el rendimiento de su aplicación abriendo un objeto **Database** conectado al origen de datos ODBC, en lugar de vincular objetos **[TableDef](tabledef-object-dao.md)** individuales a tablas específicas en el origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="08c1d-146">When you access a Microsoft access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual **[TableDef](tabledef-object-dao.md)** objects to specific tables in the ODBC data source.</span></span>

## <a name="example"></a><span data-ttu-id="08c1d-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08c1d-147">Example</span></span>

<span data-ttu-id="08c1d-148">En este ejemplo se usa el método **OpenDatabase** para abrir una base de datos de Microsoft Access y dos bases de datos ODBC conectadas por el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="08c1d-148">This example uses the **OpenDatabase** method to open one Microsoft Access database and two Microsoft Access database engine-connected ODBC databases.</span></span>

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

