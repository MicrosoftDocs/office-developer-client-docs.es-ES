---
title: Método Workspace.OpenConnection (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 9d97f298-a2d5-3b91-2efd-57f06fbd4654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198249(v=office.15)
ms:contentKeyID: 48546628
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70bdded6c149aa7aff405c769ba4462a46c20dfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308340"
---
# <a name="workspaceopenconnection-method-dao"></a><span data-ttu-id="eb2b7-102">Método Workspace.OpenConnection (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb2b7-102">Workspace.OpenConnection method (DAO)</span></span>

<span data-ttu-id="eb2b7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb2b7-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2b7-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb2b7-104">Syntax</span></span>

<span data-ttu-id="eb2b7-105">*expresión* . OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span><span class="sxs-lookup"><span data-stu-id="eb2b7-105">*expression* .OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="eb2b7-106">*expression* Variable que representa un objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-106">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb2b7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="eb2b7-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb2b7-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="eb2b7-108">Name</span></span></p></th>
<th><p><span data-ttu-id="eb2b7-109">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="eb2b7-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="eb2b7-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="eb2b7-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="eb2b7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb2b7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb2b7-112"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="eb2b7-112"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="eb2b7-113">Required</span></span></p></td>
<td><p><span data-ttu-id="eb2b7-114"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-114"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-115">Expresión de cadena.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-115">A string expression.</span></span> <span data-ttu-id="eb2b7-116">Vea la descripción en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-116">See the discussion under Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb2b7-117"><em>Opciones</em></span><span class="sxs-lookup"><span data-stu-id="eb2b7-117"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="eb2b7-118">Optional</span></span></p></td>
<td><p><span data-ttu-id="eb2b7-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-p102">Establece varias opciones para la conexión, tal como se especifica en Comentarios. Basándose en este valor, el administrador de controladores ODBC solicita al usuario información de la conexión como el nombre de origen de datos (DSN), el nombre de usuario y la contraseña.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-p102">sets various options for the connection, as specified in Remarks. Based on this value, the ODBC driver manager prompts the user for connection information such as data source name (DSN), user name, and password.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb2b7-122"><em>ReadOnly</em></span><span class="sxs-lookup"><span data-stu-id="eb2b7-122"><em>ReadOnly</em></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="eb2b7-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="eb2b7-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-125"><strong>True</strong> si la conexión se va a abrir para un acceso de sólo lectura y <strong>False</strong>, si se va a abrir para un acceso de lectura/escritura (opción predeterminada).</span><span class="sxs-lookup"><span data-stu-id="eb2b7-125"><strong>True</strong> if the connection is to be opened for read-only access and <strong>False</strong> if the connection is to be opened for read/write access (default).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb2b7-126"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="eb2b7-126"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="eb2b7-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="eb2b7-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-129">Una cadena de conexión ODBC.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-129">An ODBC connection string.</span></span> <span data-ttu-id="eb2b7-130">Vea la <strong><a href="connection-connect-property-dao.md">propiedad Connect</a></strong> para ver los elementos y la sintaxis específicos de esta cadena.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-130">See the <strong><a href="connection-connect-property-dao.md">Connect</a></strong> property for the specific elements and syntax of this string.</span></span> <span data-ttu-id="eb2b7-131">Odbc &quot; anteponer; &quot; es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-131">A prepended &quot;ODBC;&quot; is required.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="eb2b7-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb2b7-132">Return value</span></span>

<span data-ttu-id="eb2b7-133">Connection</span><span class="sxs-lookup"><span data-stu-id="eb2b7-133">Connection</span></span>

## <a name="remarks"></a><span data-ttu-id="eb2b7-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb2b7-134">Remarks</span></span>

<span data-ttu-id="eb2b7-p104">Utilice el método **OpenConnection** para establecer una conexión con un origen de datos ODBC desde un área de trabajo de ODBCDirect. El método **OpenConnection** es similar pero no equivalente a **OpenDatabase**. La diferencia principal es que **OpenConnection** sólo está disponible en un área de trabajo de ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-p104">Use the **OpenConnection** method to establish a connection to an ODBC data source from an ODBCDirect workspace. The **OpenConnection** method is similar but not equivalent to **OpenDatabase**. The main difference is that **OpenConnection** is available only in an ODBCDirect workspace.</span></span>

<span data-ttu-id="eb2b7-138">Si especifica un nombre de origen de datos ODBC (DSN) registrado en el argumento connect, el argumento name puede ser cualquier cadena válida y también proporcionará la propiedad **Name** para el objeto **Connection.**</span><span class="sxs-lookup"><span data-stu-id="eb2b7-138">If you specify a registered ODBC data source name (DSN) in the connect argument, then the name argument can be any valid string, and will also provide the **Name** property for the **Connection** object.</span></span> <span data-ttu-id="eb2b7-139">Si no se incluye un DSN válido en el argumento connect, el nombre debe hacer referencia a un DSN ODBC válido, que también será la **propiedad Name.**</span><span class="sxs-lookup"><span data-stu-id="eb2b7-139">If a valid DSN is not included in the connect argument, then name must refer to a valid ODBC DSN, which will also be the **Name** property.</span></span> <span data-ttu-id="eb2b7-140">Si ni el nombre ni la conexión contienen un DSN válido, se puede establecer el administrador de controladores ODBC (mediante el argumento options) para solicitar al usuario la información de conexión necesaria.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-140">If neither name nor connect contains a valid DSN, the ODBC driver manager can be set (via the options argument) to prompt the user for the required connection information.</span></span> <span data-ttu-id="eb2b7-141">El DSN suministrado a través de la pregunta proporciona luego la propiedad **Name**.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-141">The DSN supplied through the prompt then provides the **Name** property.</span></span>

<span data-ttu-id="eb2b7-142">El argumento options determina si se debe solicitar al usuario que establezca la conexión y cuándo se debe establecer, y si se debe abrir o no la conexión de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-142">The options argument determines if and when to prompt the user to establish the connection, and whether or not to open the connection asynchronously.</span></span> <span data-ttu-id="eb2b7-143">Puede utilizar una de las constantes siguientes.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-143">You can use one of the following constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb2b7-144">Constante</span><span class="sxs-lookup"><span data-stu-id="eb2b7-144">Constant</span></span></p></th>
<th><p><span data-ttu-id="eb2b7-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb2b7-145">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb2b7-146"><strong>dbDriverNoPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-146"><strong>dbDriverNoPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-147">El administrador de controladores ODBC utiliza la cadena de conexión proporcionada en <em>dbname</em> y <em>connect</em>.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-147">The ODBC Driver Manager uses the connection string provided in <em>dbname</em> and <em>connect</em>.</span></span> <span data-ttu-id="eb2b7-148">Si no proporciona suficiente información, se produce un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-148">If you don't provide sufficient information, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb2b7-149"><strong>dbDriverPrompt</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-149"><strong>dbDriverPrompt</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-p108">El administrador de controladores ODBC muestra el cuadro de diálogo <strong>Orígenes de datos ODBC</strong>, que indica cualquier información pertinente proporcionada en <em>dbname</em> o <em>connect</em>. La cadena de conexión está constituida por el DSN que el usuario selecciona en los cuadros de diálogo, o, si el usuario no especifica un DSN, se utiliza el DSN predeterminado.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-p108">The ODBC Driver Manager displays the <strong>ODBC Data Sources</strong> dialog box, which displays any relevant information supplied in <em>dbname</em> or <em>connect</em>. The connection string is made up of the DSN that the user selects via the dialog boxes, or, if the user doesn't specify a DSN, the default DSN is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb2b7-152"><strong>dbDriverComplete</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-152"><strong>dbDriverComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-p109">Opción predeterminada. Si el argumento <em>connect</em> incluye toda la información necesaria para completar una conexión, el administrador de controladores ODBC utiliza la cadena de <em>connect</em>. Si no, se comporta como suele hacerlo cuando especifica <strong>dbDriverPrompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-p109">Default. If the <em>connect</em> argument includes all the necessary information to complete a connection, the ODBC Driver Manager uses the string in <em>connect</em>. Otherwise it behaves as it does when you specify <strong>dbDriverPrompt</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb2b7-156"><strong>dbDriverCompleteRequired</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-156"><strong>dbDriverCompleteRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-157">Esta opción se comporta igual que <strong>dbDriverComplete</strong> excepto que el controlador ODBC deshabilita las preguntas sobre cualquier información que no sea necesaria para completar la conexión.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-157">This option behaves like <strong>dbDriverComplete</strong> except the ODBC driver disables the prompts for any information not required to complete the connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eb2b7-158"><strong>dbRunAsync</strong></span><span class="sxs-lookup"><span data-stu-id="eb2b7-158"><strong>dbRunAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="eb2b7-159">Ejecuta el método de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-159">Execute the method asynchronously.</span></span> <span data-ttu-id="eb2b7-160">Esta constante se puede utilizar con cualquiera de las demás constantes <em>options</em>.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-160">This constant may be used with any of the other <em>options</em> constants.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="eb2b7-p111">**OpenConnection** devuelve un objeto **Connection** que contiene información acerca de la conexión. El objeto **Connection** es similar al objeto **[Database](database-object-dao.md)**. La principal diferencia es que el objeto **Database** suele representar una base de datos, aunque también se puede utilizar para representar una conexión con un origen de datos ODBC desde un área de trabajo de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-p111">**OpenConnection** returns a **Connection** object which contains information about the connection. The **Connection** object is similar to a **[Database](database-object-dao.md)** object. The principal difference is that a **Database** object usually represents a database, although it can be used to represent a connection to an ODBC data source from a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="eb2b7-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eb2b7-164">Example</span></span>

<span data-ttu-id="eb2b7-165">En este ejemplo se utiliza el método **OpenConnection** con distintos parámetros para abrir tres objetos **Connection** diferentes.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-165">This example uses the **OpenConnection** method with different parameters to open three different **Connection** objects.</span></span>

```vb 
Sub OpenConnectionX() 
 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conPubs3 As Connection 
 Dim conLoop As Connection 
 
 ' Create ODBCDirect Workspace object. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Open Connection object using supplied information in 
 ' the connect string. If this information were 
 ' insufficient, you could trap for an error rather than 
 ' go to an ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection1..." 
 
 ' Note: The DSN referenced below must be set to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", _ 
 dbDriverNoPrompt, , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Open read-only Connection object based on information 
 ' you enter in the ODBC Driver Manager dialog box. 
 MsgBox "Opening Connection2..." 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", _ 
 dbDriverPrompt, True, "ODBC;DSN=Publishers;") 
 
 ' Open read-only Connection object by entering only the 
 ' missing information in the ODBC Driver Manager dialog 
 ' box. 
 MsgBox "Opening Connection3..." 
 Set conPubs3 = wrkODBC.OpenConnection("Connection3", _ 
 dbDriverCompleteRequired, True, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers;") 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 conPubs.Close 
 conPubs2.Close 
 conPubs3.Close 
 wrkODBC.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="eb2b7-166">En este ejemplo se demuestra el objeto **Connection** y la colección **Connections** abriendo un objeto **Database** de Microsoft Access y dos objetos **Connection** ODBCDirect y listando las propiedades disponibles para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="eb2b7-166">This example demonstrates the **Connection** object and **Connections** collection by opening a Microsoft Access **Database** object and two ODBCDirect **Connection** objects and listing the properties available to each object.</span></span>

```vb 
Sub ConnectionObjectX() 
 
 Dim wrkAcc as Workspace 
 Dim dbsNorthwind As Database 
 Dim wrkODBC As Workspace 
 Dim conPubs As Connection 
 Dim conPubs2 As Connection 
 Dim conLoop As Connection 
 Dim prpLoop As Property 
 
 ' Open Microsoft Access Database object. 
 Set wrkAcc = CreateWorkspace("NewWorkspace", _ 
 "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Create ODBCDirect Workspace object and open Connection 
 ' objects. 
 Set wrkODBC = CreateWorkspace("NewODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSNs referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conPubs = wrkODBC.OpenConnection("Connection1", , , _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Set conPubs2 = wrkODBC.OpenConnection("Connection2", , _ 
 True, "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 Debug.Print "Database properties:" 
 
 With dbsNorthwind 
 ' Enumerate Properties collection of Database object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop.Value 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 
 ' Enumerate the Connections collection. 
 For Each conLoop In wrkODBC.Connections 
 Debug.Print "Connection properties for " & _ 
 conLoop.Name & ":" 
 
 With conLoop 
 ' Print property values by explicitly calling each 
 ' Property object; the Connection object does not 
 ' support a Properties collection. 
 Debug.Print " Connect = " & .Connect 
 ' Property actually returns a Database object. 
 Debug.Print " Database[.Name] = " & _ 
 .Database.Name 
 Debug.Print " Name = " & .Name 
 Debug.Print " QueryTimeout = " & .QueryTimeout 
 Debug.Print " RecordsAffected = " & _ 
 .RecordsAffected 
 Debug.Print " StillExecuting = " & _ 
 .StillExecuting 
 Debug.Print " Transactions = " & .Transactions 
 Debug.Print " Updatable = " & .Updatable 
 End With 
 
 Next conLoop 
 
 dbsNorthwind.Close 
 conPubs.Close 
 conPubs2.Close 
 wrkAcc.Close 
 wrkODBC.Close 
 
End Sub 
 
```

