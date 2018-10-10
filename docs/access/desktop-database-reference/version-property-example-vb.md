---
title: Ejemplo de la propiedad Version (VB)
TOCTitle: Version Property Example (VB)
ms:assetid: ffb7b04a-55b9-fa2f-41ec-44af225bd15f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250315(v=office.15)
ms:contentKeyID: 48548968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159a8c29db34c432ecd332c489ad3917eab00416
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484897"
---
# <a name="version-property-example-vb"></a><span data-ttu-id="4c128-102">Ejemplo de la propiedad Version (VB)</span><span class="sxs-lookup"><span data-stu-id="4c128-102">Version Property Example (VB)</span></span>


<span data-ttu-id="4c128-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c128-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c128-p101">En este ejemplo se usa la propiedad [Version](version-property-ado.md) de un objeto [Connection](connection-object-ado.md) para mostrar la versión de ADO actual. También se usan varias propiedades dinámicas para mostrar:</span><span class="sxs-lookup"><span data-stu-id="4c128-p101">This example uses the [Version](version-property-ado.md) property of a [Connection](connection-object-ado.md) object to display the current ADO version. It also uses several dynamic properties to show:</span></span>

  - <span data-ttu-id="4c128-106">El nombre DBMS y la versión actuales.</span><span class="sxs-lookup"><span data-stu-id="4c128-106">the current DBMS name and version.</span></span>

  - <span data-ttu-id="4c128-107">La versión de OLE DB.</span><span class="sxs-lookup"><span data-stu-id="4c128-107">OLE DB version.</span></span>

  - <span data-ttu-id="4c128-108">El nombre del proveedor y la versión.</span><span class="sxs-lookup"><span data-stu-id="4c128-108">provider name and version.</span></span>

  - <span data-ttu-id="4c128-109">La versión de ODBC.</span><span class="sxs-lookup"><span data-stu-id="4c128-109">ODBC version.</span></span>

  - <span data-ttu-id="4c128-110">El nombre del controlador ODBC y la versión.</span><span class="sxs-lookup"><span data-stu-id="4c128-110">ODBC driver name and version.</span></span>

<!-- end list -->

```vb 
 
'BeginVersionVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strVersionInfo As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 strVersionInfo = "ADO Version: " & Cnxn.Version & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Name: " & Cnxn.Properties("DBMS Name") & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Version: " & Cnxn.Properties("DBMS Version") & vbCr 
 strVersionInfo = strVersionInfo & "OLE DB Version: " & Cnxn.Properties("OLE DB Version") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Name: " & Cnxn.Properties("Provider Name") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Version: " & Cnxn.Properties("Provider Version") & vbCr 
 
 MsgBox strVersionInfo 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndVersionVB 
```

