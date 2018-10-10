---
title: Obtener acceso a las filas de un objeto Recordset jerárquico
TOCTitle: Accessing Rows in a Hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a7596341f96c7df1d51e67721aacd15f8b075f25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486516"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>Obtener acceso a las filas de un objeto Recordset jerárquico


**Se aplica a**: Access 2013 | Office 2013

En el ejemplo siguiente, se muestran los pasos necesarios para obtener acceso a filas de un objeto [Recordset](recordset-object-ado.md) jerárquico:

1.  Los objetos **Recordset** de las tablas authors y titleauthor están relacionados por identificador de autor.

2.  El bucle externo muestra el nombre y apellido, el estado y la identificación de cada autor.

3.  El objeto **Recordset** anexado para cada fila se recupera de la colección **Fields** y se asigna a *rstTitleAuthor*.

4.  El bucle interno muestra cuatro campos de cada fila en el objeto **Recordset** anexado.

(La propiedad [StayInSync](stayinsync-property-ado.md) se establece en FALSE (falso) como ejemplo, de modo que se pueda ver el cambio de capítulo explícitamente en cada iteración del bucle externo. Sin embargo, el ejemplo será más eficiente si la asignación en el paso 3 se traslada antes de la primera línea del paso 2, para que la asignación sólo se realice una vez. A continuación, establezca la propiedad **StayInSync** en TRUE, para que *rstTitleAuthor* cambie implícita y automáticamente al capítulo correspondiente siempre que *rst* pase a una nueva fila.)

**Ejemplo**

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

