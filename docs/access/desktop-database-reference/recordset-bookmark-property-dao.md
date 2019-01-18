---
title: Propiedad Recordset.Bookmark (DAO)
TOCTitle: Bookmark Property
ms:assetid: c4b1c2d9-668e-e365-544c-efb4ae4efcc9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823084(v=office.15)
ms:contentKeyID: 48547597
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052887
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 1ebf963695b2d754a4501077e2236c52280a9a2e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714531"
---
# <a name="recordsetbookmark-property-dao"></a><span data-ttu-id="11a89-102">Propiedad Recordset.Bookmark (DAO)</span><span class="sxs-lookup"><span data-stu-id="11a89-102">Recordset.Bookmark property (DAO)</span></span>


<span data-ttu-id="11a89-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11a89-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11a89-104">Establece o devuelve un marcador que identifica de forma exclusiva el registro actual de un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="11a89-104">Sets or returns a bookmark that uniquely identifies the current record in a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11a89-105">Syntax</span></span>

<span data-ttu-id="11a89-106">*expresión* . Marcador</span><span class="sxs-lookup"><span data-stu-id="11a89-106">*expression* .Bookmark</span></span>

<span data-ttu-id="11a89-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="11a89-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="11a89-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11a89-108">Remarks</span></span>

<span data-ttu-id="11a89-109">Para un objeto **Recordset** basado completamente en tablas del motor de base de datos de Microsoft Access, el valor de la propiedad **Bookmarkable** es True y puede utilizar la propiedad **Bookmark** con ese **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="11a89-109">For a **Recordset** object based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use the **Bookmark** property with that **Recordset**.</span></span> <span data-ttu-id="11a89-110">Sin embargo, puede que otros productos de base de datos no admitan marcadores.</span><span class="sxs-lookup"><span data-stu-id="11a89-110">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="11a89-111">Por ejemplo, no se pueden usar marcadores en un objeto **Recordset** basado en una tabla vinculada de Paradox que no tenga una clave principal.</span><span class="sxs-lookup"><span data-stu-id="11a89-111">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

<span data-ttu-id="11a89-p102">Cuando se crea o se abre un objeto **Recordset**, cada registro tiene ya un marcador único. Puede guardar el marcador del registro actual asignando el valor de la propiedad **Bookmark** a una variable. Para poder volver rápidamente a ese registro después de moverse a otro, establezca la propiedad **Bookmark** del objeto **Recordset** en el valor de dicha variable.</span><span class="sxs-lookup"><span data-stu-id="11a89-p102">When you create or open a **Recordset** object, each of its records already has a unique bookmark. You can save the bookmark for the current record by assigning the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="11a89-p103">No hay límite en el número de marcadores que se pueden establecer. Para crear un marcador para un registro distinto del actual, desplácese al registro deseado y asigne el valor de la propiedad **Bookmark** a una variable de tipo **String** que identifique el registro.</span><span class="sxs-lookup"><span data-stu-id="11a89-p103">There is no limit to the number of bookmarks you can establish. To create a bookmark for a record other than the current record, move to the desired record and assign the value of the **Bookmark** property to a **String** variable that identifies the record.</span></span>

<span data-ttu-id="11a89-117">Para asegurarse de que el objeto **Recordset** admita marcadores, compruebe el valor de su propiedad **[Bookmarkable](recordset-bookmarkable-property-dao.md)** antes de usar la propiedad **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="11a89-117">To make sure the **Recordset** object supports bookmarks, check the value of its **[Bookmarkable](recordset-bookmarkable-property-dao.md)** property before you use the **Bookmark** property.</span></span> <span data-ttu-id="11a89-118">Si la propiedad **Bookmarkable** es False, el objeto **Recordset** no admite marcadores y, mediante el **marcador** de propiedad da como resultado un error capturable.</span><span class="sxs-lookup"><span data-stu-id="11a89-118">If the **Bookmarkable** property is False, the **Recordset** object doesn't support bookmarks, and using the **Bookmark** property results in a trappable error.</span></span>

<span data-ttu-id="11a89-p105">Si usa el método **[Clone](recordset-clone-method-dao.md)** para crear una copia de un objeto **Recordset**, la configuración de la propiedad **Bookmark** de los objetos **Recordset** original y duplicado es idéntica y se puede usar indistintamente. Sin embargo, no se pueden usar marcadores de distintos objetos **Recordset** indistintamente, incluso si se crearon mediante el mismo objeto o la misma instrucción SQL.</span><span class="sxs-lookup"><span data-stu-id="11a89-p105">If you use the **[Clone](recordset-clone-method-dao.md)** method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and can be used interchangeably. However, you can't use bookmarks from different **Recordset** objects interchangeably, even if they were created by using the same object or the same SQL statement.</span></span>

<span data-ttu-id="11a89-121">Si se establece la propiedad **Bookmark** en un valor que representa un registro eliminado, se produce un error capturable.</span><span class="sxs-lookup"><span data-stu-id="11a89-121">If you set the **Bookmark** property to a value that represents a deleted record, a trappable error occurs.</span></span>

<span data-ttu-id="11a89-122">El valor de la propiedad **Bookmark** no es lo mismo que el número de registro.</span><span class="sxs-lookup"><span data-stu-id="11a89-122">The value of the **Bookmark** property isn't the same as a record number.</span></span>

## <a name="example"></a><span data-ttu-id="11a89-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11a89-123">Example</span></span>

<span data-ttu-id="11a89-124">En este ejemplo, se usan las propiedades **Bookmark** y **Bookmarkable** para permitir que el usuario marque un registro de un objeto **Recordset** y vuelva a él más adelante.</span><span class="sxs-lookup"><span data-stu-id="11a89-124">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset 
     Dim strMessage As String 
     Dim intCommand As Integer 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCategories = _ 
     dbsNorthwind.OpenRecordset("Categories", _ 
     dbOpenSnapshot) 
     
     With rstCategories 
     
     If .Bookmarkable = False Then 
     Debug.Print "Recordset is not Bookmarkable!" 
     Else 
     ' Populate Recordset. 
     .MoveLast 
     .MoveFirst 
     
     Do While True 
     ' Show information about current record and get 
     ' user input. 
     strMessage = "Category: " & !CategoryName & _ 
     " (record " & (.AbsolutePosition + 1) & _ 
     " of " & .RecordCount & ")" & vbCr & _ 
     "Enter command:" & vbCr & _ 
     "[1 - next / 2 - previous /" & vbCr & _ 
     "3 - set bookmark / 4 - go to bookmark]" 
     intCommand = Val(InputBox(strMessage)) 
     
     Select Case intCommand 
     ' Move forward or backward, trapping for BOF 
     ' or EOF. 
     Case 1 
     .MoveNext 
     If .EOF Then .MoveLast 
     Case 2 
     .MovePrevious 
     If .BOF Then .MoveFirst 
     
     ' Store the bookmark of the current record. 
     Case 3 
     varBookmark = .Bookmark 
     
     ' Go to the record indicated by the stored 
     ' bookmark. 
     Case 4 
     If IsEmpty(varBookmark) Then 
     MsgBox "No Bookmark set!" 
     Else 
     .Bookmark = varBookmark 
     End If 
     
     Case Else 
     Exit Do 
     End Select 
     
     Loop 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="11a89-125">En este ejemplo se utiliza la propiedad **LastModified** para mover el puntero de registros actual a ambos registros, al que se ha modificado y al que se ha creado recientemente.</span><span class="sxs-lookup"><span data-stu-id="11a89-125">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
