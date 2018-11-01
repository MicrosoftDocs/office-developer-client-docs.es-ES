---
title: Colección Views, propiedad CommandText (VB)
TOCTitle: Views Collection, CommandText property example (VB)
ms:assetid: 5dacd3c2-a1b2-57a7-1bac-ce0caa7c1a09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249331(v=office.15)
ms:contentKeyID: 48545120
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab1d5013e0371273fdcec3b2ba75a30a8dc18393
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870544"
---
# <a name="views-collection-commandtext-property-example-vb"></a><span data-ttu-id="2a9e4-102">Colección Views, propiedad CommandText (VB)</span><span class="sxs-lookup"><span data-stu-id="2a9e4-102">Views Collection, CommandText property example (VB)</span></span>


<span data-ttu-id="2a9e4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a9e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2a9e4-104">El código siguiente muestra cómo utilizar la propiedad [Comando](command-property-adox.md) para actualizar el texto de una vista.</span><span class="sxs-lookup"><span data-stu-id="2a9e4-104">The following code demonstrates how to use the [Command](command-property-adox.md) property to update the text of a view.</span></span>

```vb 
 
' BeginViewsCollectionVB 
Sub Main() 
 On Error GoTo ViewTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command 
 Set cmd = cat.Views("AllCustomers").Command 
 
 ' Update the CommandText of the Command 
 cmd.CommandText = _ 
 "Select CustomerId, CompanyName, ContactName From Customers" 
 
 ' Update the View 
 Set cat.Views("AllCustomers").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ViewTextError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndViewsCollectionVB 
```

