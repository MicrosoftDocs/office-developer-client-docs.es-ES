---
title: Propiedad Recordset.Bookmarkable (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 6323f162-75c4-7cfe-c918-0b9454560f97
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194950(v=office.15)
ms:contentKeyID: 48545257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fda41958b769c274564655b5bab2789f06e64682
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924655"
---
# <a name="recordsetbookmarkable-property-dao"></a><span data-ttu-id="4b6ad-102">Propiedad Recordset.Bookmarkable (DAO)</span><span class="sxs-lookup"><span data-stu-id="4b6ad-102">Recordset.Bookmarkable property (DAO)</span></span>


<span data-ttu-id="4b6ad-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b6ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b6ad-104">Devuelve un valor que indica si un objeto **Recordset** admite marcadores, que se pueden establecer mediante la propiedad **[Bookmark](recordset-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b6ad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b6ad-105">Syntax</span></span>

<span data-ttu-id="4b6ad-106">*expresión* . Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="4b6ad-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="4b6ad-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="4b6ad-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b6ad-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b6ad-108">Remarks</span></span>

<span data-ttu-id="4b6ad-109">Compruebe el valor de la propiedad **Bookmarkable** de un objeto **Recordset** antes de intentar establecer o comprobar la propiedad **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="4b6ad-110">Para los objetos **Recordset** basados completamente en tablas del motor de base de datos de Microsoft Access, el valor de la propiedad **Bookmarkable** es True y puede utilizar marcadores.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="4b6ad-111">Sin embargo, puede que otros productos de base de datos no admitan marcadores.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="4b6ad-112">Por ejemplo, no se pueden usar marcadores en un objeto **Recordset** basado en una tabla vinculada de Paradox que no tenga una clave principal.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="4b6ad-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b6ad-113">Example</span></span>

<span data-ttu-id="4b6ad-114">En este ejemplo, se usan las propiedades **Bookmark** y **Bookmarkable** para permitir que el usuario marque un registro de un objeto **Recordset** y vuelva a él más adelante.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a **Recordset** and return to it later.</span></span>

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
