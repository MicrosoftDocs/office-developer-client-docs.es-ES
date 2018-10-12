---
title: Recordset.Clone Method (DAO)
TOCTitle: Clone Method
ms:assetid: 50cbc011-7e72-4dee-488d-96e681618e8e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193824(v=office.15)
ms:contentKeyID: 48544802
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052909
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 37f78b428cc4f872743fe39403608074460b276a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485585"
---
# <a name="recordsetclone-method-dao"></a><span data-ttu-id="9acaf-102">Recordset.Clone Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="9acaf-102">Recordset.Clone Method (DAO)</span></span>


<span data-ttu-id="9acaf-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9acaf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9acaf-104">Crea un objeto **[Recordset](recordset-object-dao.md)** duplicado que hace referencia al objeto **Recordset** original.</span><span class="sxs-lookup"><span data-stu-id="9acaf-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acaf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9acaf-105">Syntax</span></span>

<span data-ttu-id="9acaf-106">*expresión* . Clone</span><span class="sxs-lookup"><span data-stu-id="9acaf-106">*expression* .Clone</span></span>

<span data-ttu-id="9acaf-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="9acaf-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="9acaf-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9acaf-108">Return Value</span></span>

<span data-ttu-id="9acaf-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="9acaf-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="9acaf-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9acaf-110">Remarks</span></span>

<span data-ttu-id="9acaf-p101">Use el método **Clone** para crear varios objetos **Recordset** duplicados. Cada objeto **Recordset** puede tener su propio registro actual. El método **Clone** por sí mismo no cambia los datos en los objetos ni en las estructuras subyacentes. Cuando use el método **Clone**, puede compartir marcadores entre dos o más objetos **Recordset**, porque sus marcadores son intercambiables.</span><span class="sxs-lookup"><span data-stu-id="9acaf-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each **Recordset** can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="9acaf-p102">Puede usar el método **Clone** cuando quiera realizar una operación en un **conjunto de registros** que requiera varios registros actuales. Es más rápido y eficaz que abrir un segundo **conjunto de registros**. Cuando se crea un **conjunto de registros** con el método **Clone**, al principio no tiene un registro actual. Para que haya un registro actual antes de usar el clon del **conjunto de registros**, debe definir la propiedad **[Bookmark](recordset-bookmark-property-dao.md)** o usar uno de los métodos **[Move](recordset-movefirst-method-dao.md)**, uno de los métodos **[Find](recordset-findfirst-method-dao.md)** o el método **[Seek](recordset-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="9acaf-p102">You can use the **Clone** method when you want to perform an operation on a **Recordset** that requires multiple current records. This is faster and more efficient than opening a second **Recordset**. When you create a **Recordset** with the **Clone** method, it initially lacks a current record. To make a record current before you use the **Recordset** clone, you must set the **[Bookmark](recordset-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset-findfirst-method-dao.md)** methods, or the **[Seek](recordset-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="9acaf-p103">El uso del método **[Close](connection-close-method-dao.md)** en el objeto original o duplicado no afecta al otro objeto. Por ejemplo, usar **Close** en el **conjunto de registros** original no cierra el clon.</span><span class="sxs-lookup"><span data-stu-id="9acaf-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original **Recordset** doesn't close the clone.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="9acaf-121">Cerrar un conjunto de registros clon con una transacción pendiente provoca una operación <STRONG>Rollback</STRONG> implícita.</span><span class="sxs-lookup"><span data-stu-id="9acaf-121">Closing a clone recordset within a pending transaction will cause an implicit <STRONG>Rollback</STRONG> operation.</span></span></P>
> <LI>
> <P><span data-ttu-id="9acaf-p104">Al clonar un objeto <STRONG>Recordset</STRONG> de tipo tabla en un área de trabajo de Microsoft Access, no se clona el valor de la propiedad <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> en la nueva copia del conjunto de registros. Debe copiar el valor de la propiedad <STRONG>Index</STRONG> manualmente.</span><span class="sxs-lookup"><span data-stu-id="9acaf-p104">When you clone a table-type <STRONG>Recordset</STRONG> object in a Microsoft Access workspace, the <STRONG><A href="recordset2-index-property-dao.md">Index</A></STRONG> property setting is not cloned on the new copy of the recordset. You must copy the <STRONG>Index</STRONG> property setting manually.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="9acaf-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9acaf-124">Example</span></span>

<span data-ttu-id="9acaf-125">En este ejemplo se usa el método **Clone** para crear copias de un **conjunto de registros** y, después, se deja que el usuario coloque el puntero de registros de cada copia de manera independiente.</span><span class="sxs-lookup"><span data-stu-id="9acaf-125">This example uses the **Clone** method to create copies of a **Recordset** and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset 
       Dim intLoop As Integer 
       Dim strMessage As String 
       Dim strFind As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' If the following SQL statement will be used often,  
       ' creating a permanent QueryDef will result in better 
       ' performance. 
       Set arstProducts(1) = dbsNorthwind.OpenRecordset( _ 
          "SELECT ProductName FROM Products " & _ 
          "ORDER BY ProductName", dbOpenSnapshot) 
     
       ' Create two clones of the original Recordset. 
       Set arstProducts(2) = arstProducts(1).Clone 
       Set arstProducts(3) = arstProducts(1).Clone 
     
       Do While True 
     
          ' Loop through the array so that on each pass, the  
          ' user is searching a different copy of the same  
          ' Recordset. 
          For intLoop = 1 To 3 
     
             ' Ask for search string while showing where the 
             ' current record pointer is for each Recordset. 
             strMessage = _ 
                "Recordsets from Products table:" & vbCr & _ 
                "  1 - Original - Record pointer at " & _ 
                arstProducts(1)!ProductName & vbCr & _ 
                "  2 - Clone - Record pointer at " & _ 
                arstProducts(2)!ProductName & vbCr & _ 
                "  3 - Clone - Record pointer at " & _ 
                arstProducts(3)!ProductName & vbCr & _ 
                "Enter search string for #" & intLoop & ":" 
             strFind = Trim(InputBox(strMessage)) 
             If strFind = "" Then Exit Do 
     
             ' Find the search string; if there's no match, jump 
             ' to the last record. 
             With arstProducts(intLoop) 
                .FindFirst "ProductName >= '" & strFind & "'" 
                If .NoMatch Then .MoveLast 
             End With 
     
          Next intLoop 
     
       Loop 
     
       arstProducts(1).Close 
       arstProducts(2).Close 
       arstProducts(3).Close 
       dbsNorthwind.Close 
     
    End Sub
```