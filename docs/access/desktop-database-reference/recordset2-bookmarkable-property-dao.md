---
title: Recordset2.Bookmarkable Property (DAO)
TOCTitle: Bookmarkable Property
ms:assetid: 9c93d04d-ca10-acf5-122a-58625ed93424
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198125(v=office.15)
ms:contentKeyID: 48546601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052888
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 969561715842e317c2518e5d8570c73bdf9920bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486778"
---
# <a name="recordset2bookmarkable-property-dao"></a><span data-ttu-id="e31eb-102">Recordset2.Bookmarkable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="e31eb-102">Recordset2.Bookmarkable Property (DAO)</span></span>


<span data-ttu-id="e31eb-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e31eb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e31eb-104">Devuelve un valor que indica si un objeto **Recordset** admite marcadores, que se pueden establecer mediante la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="e31eb-104">Returns a value that indicates whether a **Recordset** object supports bookmarks, which you can set by using the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31eb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e31eb-105">Syntax</span></span>

<span data-ttu-id="e31eb-106">*expresión* . Bookmarkable</span><span class="sxs-lookup"><span data-stu-id="e31eb-106">*expression* .Bookmarkable</span></span>

<span data-ttu-id="e31eb-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="e31eb-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e31eb-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e31eb-108">Remarks</span></span>

<span data-ttu-id="e31eb-109">Compruebe el valor de la propiedad **Bookmarkable** de un objeto **Recordset** antes de intentar establecer o comprobar la propiedad **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="e31eb-109">Check the **Bookmarkable** property setting of a **Recordset** object before you attempt to set or check the **Bookmark** property.</span></span>

<span data-ttu-id="e31eb-110">Para los objetos **Recordset** basados completamente en tablas del motor de base de datos de Microsoft Access, el valor de la propiedad **Bookmarkable** es True y puede utilizar marcadores.</span><span class="sxs-lookup"><span data-stu-id="e31eb-110">For **Recordset** objects based entirely on Microsoft Access database engine tables, the value of the **Bookmarkable** property is True, and you can use bookmarks.</span></span> <span data-ttu-id="e31eb-111">Sin embargo, puede que otros productos de base de datos no admitan marcadores.</span><span class="sxs-lookup"><span data-stu-id="e31eb-111">Other database products may not support bookmarks, however.</span></span> <span data-ttu-id="e31eb-112">Por ejemplo, no se pueden usar marcadores en un objeto **Recordset** basado en una tabla vinculada de Paradox que no tenga una clave principal.</span><span class="sxs-lookup"><span data-stu-id="e31eb-112">For example, you can't use bookmarks in any **Recordset** object based on a linked Paradox table that has no primary key.</span></span>

## <a name="example"></a><span data-ttu-id="e31eb-113">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e31eb-113">Example</span></span>

<span data-ttu-id="e31eb-114">En este ejemplo se utilizan las propiedades **Bookmark** y **Bookmarkable** para que el usuario pueda marcar un registro en un conjunto de registros y volver al mismo más adelante.</span><span class="sxs-lookup"><span data-stu-id="e31eb-114">This example uses the **Bookmark** and **Bookmarkable** properties to let the user flag a record in a recordset and return to it later.</span></span>

```vb
    Sub BookmarkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCategories As Recordset2 
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