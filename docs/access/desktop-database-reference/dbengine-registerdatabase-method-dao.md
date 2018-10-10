---
title: DBEngine.RegisterDatabase Method (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 304f517d11e6e333bb0455e3882421c410c56b72
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484312"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="7cb1f-102">DBEngine.RegisterDatabase Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="7cb1f-102">DBEngine.RegisterDatabase Method (DAO)</span></span>


<span data-ttu-id="7cb1f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7cb1f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="7cb1f-p101">Proporciona información de conexión para un origen de datos ODBC en el Registro de Windows. El controlador ODBC necesita información de conexión cuando se abre el origen de datos ODBC durante una sesión.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-p101">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb1f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cb1f-106">Syntax</span></span>

<span data-ttu-id="7cb1f-107">*expresión* . RegisterDatabase (***Dsn***, ***controlador***, ***silenciosa***, ***atributos***)</span><span class="sxs-lookup"><span data-stu-id="7cb1f-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="7cb1f-108">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="7cb1f-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="7cb1f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7cb1f-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7cb1f-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="7cb1f-110">Name</span></span></p></th>
<th><p><span data-ttu-id="7cb1f-111">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="7cb1f-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="7cb1f-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="7cb1f-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="7cb1f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cb1f-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7cb1f-114">DSN</span><span class="sxs-lookup"><span data-stu-id="7cb1f-114">Dsn</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7cb1f-115">Required</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7cb1f-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7cb1f-p102">Nombre utilizado en el método <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong>. Se refiere a un bloque de información descriptiva sobre el origen de datos. Por ejemplo, si el origen de datos es una base de datos remota ODBC, podría ser el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-p102">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method. It refers to a block of descriptive information about the data source. For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb1f-120">Controlador</span><span class="sxs-lookup"><span data-stu-id="7cb1f-120">Driver</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7cb1f-121">Required</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7cb1f-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7cb1f-p103">Nombre del controlador ODBC. Éste no es el nombre del archivo DLL del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-p103">The name of the ODBC driver. This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7cb1f-125">Silenciosa</span><span class="sxs-lookup"><span data-stu-id="7cb1f-125">Silent</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-126">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7cb1f-126">Required</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="7cb1f-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="7cb1f-128"><strong>True</strong> si no desea mostrar los cuadros de diálogo del controlador ODBC que solicitan información específica del controlador; o <strong>False</strong> si desea mostrar los cuadros de diálogo del controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="7cb1f-129">Si silent es <strong>True</strong>, attributes debe contener toda la información necesaria específica del controlador o se muestran los cuadros de diálogo de todos modos.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7cb1f-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="7cb1f-130">Attributes</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-131">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7cb1f-131">Required</span></span></p></td>
<td><p><span data-ttu-id="7cb1f-132"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7cb1f-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7cb1f-p105">Lista de palabras clave que se deben agregar al Registro de Windows. Las palabras clave están en una cadena delimitada por retornos de carro.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-p105">A list of keywords to be added to the Windows Registry. The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7cb1f-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cb1f-135">Remarks</span></span>

<span data-ttu-id="7cb1f-136">Si la base de datos ya está registrada (ya se ha proporcionado la información de conexión) en el Registro de Windows cuando utiliza el método **RegisterDatabase**, la información de conexión está actualizada.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="7cb1f-137">Si el método **RegisterDatabase** provoca un error por algún motivo, no se han realizado cambios en el Registro de Windows y se produce un error.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="7cb1f-138">Para obtener más información sobre los controladores ODBC como SQL Server, vea el archivo de Ayuda suministrado con el controlador.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="7cb1f-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7cb1f-139">Example</span></span>

<span data-ttu-id="7cb1f-140">En este ejemplo se utiliza el método **RegisterDatabase** para registrar un origen de datos Microsoft SQL llamado Publishers en el Registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

