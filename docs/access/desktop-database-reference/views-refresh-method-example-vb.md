---
title: Ejemplo del método Refresh de Views (VB)
TOCTitle: Views Refresh method example (VB)
ms:assetid: 607b78d6-1b26-d643-9f97-f47b5f5cffc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249352(v=office.15)
ms:contentKeyID: 48545182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 167930a29c040f9394f72ee3b2be158555e96edf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25866967"
---
# <a name="views-refresh-method-example-vb"></a><span data-ttu-id="4c764-102">Ejemplo del método Refresh de Views (VB)</span><span class="sxs-lookup"><span data-stu-id="4c764-102">Views Refresh method example (VB)</span></span>


<span data-ttu-id="4c764-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c764-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c764-p101">El código siguiente muestra cómo actualizar la colección [Views](views-collection-adox.md) de un [catálogo](catalog-object-adox.md). Esto es necesario para poder tener acceso a objetos [View](view-object-adox.md) del **catálogo**.</span><span class="sxs-lookup"><span data-stu-id="4c764-p101">The following code shows how to refresh the [Views](views-collection-adox.md) collection of a [Catalog](catalog-object-adox.md). This is required before [View](view-object-adox.md) objects from the **Catalog** can be accessed.</span></span>

```vb 
 
' BeginViewsRefreshVB 
Sub Main() 
 On Error GoTo ProcedureViewsRefreshError 
 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Refresh the Procedures collection 
 cat.Views.Refresh 
 
 'Clean up 
 Set cat = Nothing 
 Exit Sub 
 
ProcedureViewsRefreshError: 
 
 If Not cat Is Nothing Then 
 Set cat = Nothing 
 End If 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndViewsRefreshVB 
```

