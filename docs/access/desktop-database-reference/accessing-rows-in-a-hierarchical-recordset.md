---
title: Acceso a las filas de un Recordset jerárquico
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 3041aa1486f9630a36383dde4ad675c50c799339
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870033"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="d93ae-102">Acceso a las filas de un Recordset jerárquico</span><span class="sxs-lookup"><span data-stu-id="d93ae-102">Accessing rows in a hierarchical Recordset</span></span>

<span data-ttu-id="d93ae-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d93ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d93ae-104">En el ejemplo siguiente, se muestran los pasos necesarios para obtener acceso a filas de un objeto [Recordset](recordset-object-ado.md) jerárquico:</span><span class="sxs-lookup"><span data-stu-id="d93ae-104">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

1. <span data-ttu-id="d93ae-105">Los objetos **Recordset** de las tablas authors y titleauthor están relacionados por identificador de autor.</span><span class="sxs-lookup"><span data-stu-id="d93ae-105">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="d93ae-106">El bucle externo muestra el nombre y apellido, el estado y la identificación de cada autor.</span><span class="sxs-lookup"><span data-stu-id="d93ae-106">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="d93ae-107">El objeto **Recordset** anexado para cada fila se recupera de la colección **Fields** y se asigna a *rstTitleAuthor*.</span><span class="sxs-lookup"><span data-stu-id="d93ae-107">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="d93ae-108">El bucle interno muestra cuatro campos de cada fila en el objeto **Recordset** anexado.</span><span class="sxs-lookup"><span data-stu-id="d93ae-108">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="d93ae-109">La propiedad [StayInSync](stayinsync-property-ado.md) se establece en FALSE para fines de ilustración, para que pueda ver el capítulo cambiar explícitamente en cada iteración del bucle externo.</span><span class="sxs-lookup"><span data-stu-id="d93ae-109">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="d93ae-110">Sin embargo, el ejemplo será más eficiente si la asignación en el paso 3 se traslada antes de la primera línea del paso 2, para que la asignación sólo se realice una vez.</span><span class="sxs-lookup"><span data-stu-id="d93ae-110">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="d93ae-111">Establezca la propiedad **StayInSync** en TRUE, para que *rstTitleAuthor* cambie implícita y automáticamente al capítulo correspondiente siempre que *rst* pase a una nueva fila.</span><span class="sxs-lookup"><span data-stu-id="d93ae-111">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>

<span data-ttu-id="d93ae-112">**Ejemplo**</span><span class="sxs-lookup"><span data-stu-id="d93ae-112">**Example**</span></span>

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

