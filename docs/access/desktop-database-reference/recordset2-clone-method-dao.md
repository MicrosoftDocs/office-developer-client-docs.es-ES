---
title: Recordset2.Clone (método) (DAO)
TOCTitle: Clone Method
ms:assetid: f0d32cb1-03f6-395d-2509-b2139a5fdc68
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836567(v=office.15)
ms:contentKeyID: 48548614
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 598944aadb344ab97d7561e7ef55a67041c4fbf1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998755"
---
# <a name="recordset2clone-method-dao"></a><span data-ttu-id="3c76f-102">Recordset2.Clone (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="3c76f-102">Recordset2.Clone method (DAO)</span></span>

<span data-ttu-id="3c76f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c76f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c76f-104">Crea un objeto **[Recordset](recordset-object-dao.md)** duplicado que hace referencia al objeto **Recordset2** original.</span><span class="sxs-lookup"><span data-stu-id="3c76f-104">Creates a duplicate **[Recordset](recordset-object-dao.md)** object that refers to the original **Recordset2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c76f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c76f-105">Syntax</span></span>

<span data-ttu-id="3c76f-106">*expresión* . Clone</span><span class="sxs-lookup"><span data-stu-id="3c76f-106">*expression* .Clone</span></span>

<span data-ttu-id="3c76f-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3c76f-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c76f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c76f-108">Return value</span></span>

<span data-ttu-id="3c76f-109">Recordset</span><span class="sxs-lookup"><span data-stu-id="3c76f-109">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="3c76f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c76f-110">Remarks</span></span>

<span data-ttu-id="3c76f-p101">Utilice el método **Clone** para crear varios objetos **Recordset** duplicados. Cada conjunto de registros puede tener su propio registro actual. Si se utiliza **Clone** por sí mismo, no se modifican los datos en los objetos o en las estructuras subyacentes. Cuando utiliza el método **Clone**, puede compartir marcadores entre dos o más objetos **Recordset2** porque sus marcadores son intercambiables.</span><span class="sxs-lookup"><span data-stu-id="3c76f-p101">Use the **Clone** method to create multiple, duplicate **Recordset** objects. Each recordset can have its own current record. Using **Clone** by itself doesn't change the data in the objects or in their underlying structures. When you use the **Clone** method, you can share bookmarks between two or more **Recordset2** objects because their bookmarks are interchangeable.</span></span>

<span data-ttu-id="3c76f-p102">Puede utilizar el método **Clone** cuando desea realizar una operación en un conjunto de registros que requiere varios registros actuales. Es más rápido y eficaz que abrir un segundo conjunto de registros. Cuando se crea un conjunto de registros con el método **Clone**, al principio no tiene un registro actual. Para que haya un registro activo antes de utilizar el clon del conjunto de registros, debe definir la propiedad **[Bookmark](recordset2-bookmark-property-dao.md)** o utilizar uno de los métodos **[Move](recordset-movefirst-method-dao.md)**, uno de los métodos **[Find](recordset2-findfirst-method-dao.md)** o el método **[Seek](recordset2-seek-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="3c76f-p102">You can use the **Clone** method when you want to perform an operation on a recordset that requires multiple current records. This is faster and more efficient than opening a second recordset. When you create a recordset with the **Clone** method, it initially lacks a current record. To make a record current before you use the recordset clone, you must set the **[Bookmark](recordset2-bookmark-property-dao.md)** property or use one of the **[Move](recordset-movefirst-method-dao.md)** methods, one of the **[Find](recordset2-findfirst-method-dao.md)** methods, or the **[Seek](recordset2-seek-method-dao.md)** method.</span></span>

<span data-ttu-id="3c76f-p103">El uso del método **[Close](connection-close-method-dao.md)** en el objeto original o duplicado no afecta al otro objeto. Por ejemplo, utilizar **Close** en el conjunto de registros original no cierra el clon.</span><span class="sxs-lookup"><span data-stu-id="3c76f-p103">Using the **[Close](connection-close-method-dao.md)** method on either the original or duplicate object doesn't affect the other object. For example, using **Close** on the original recordset doesn't close the clone.</span></span>

> [!NOTE]
> - <span data-ttu-id="3c76f-121">Cerrar un conjunto de registros clon con una transacción pendiente provoca una operación **Rollback** implícita.</span><span class="sxs-lookup"><span data-stu-id="3c76f-121">Closing a clone recordset within a pending transaction will cause an implicit **Rollback** operation.</span></span>
> - <span data-ttu-id="3c76f-p104">Al clonar un objeto **Recordset** de tipo tabla en un área de trabajo de Microsoft Access, no se clona el valor de la propiedad **[Index](recordset2-index-property-dao.md)** en la nueva copia del conjunto de registros. Debe copiar el valor de la propiedad **Index** manualmente.</span><span class="sxs-lookup"><span data-stu-id="3c76f-p104">When you clone a table-type **Recordset** object in a Microsoft Access workspace, the **[Index](recordset2-index-property-dao.md)** property setting is not cloned on the new copy of the recordset. You must copy the **Index** property setting manually.</span></span>

## <a name="example"></a><span data-ttu-id="3c76f-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3c76f-124">Example</span></span>

<span data-ttu-id="3c76f-125">En este ejemplo se utiliza el método **Clone** para crear copias de un conjunto de registros y, a continuación, se deja que el usuario coloque el puntero de registros de cada copia de manera independiente.</span><span class="sxs-lookup"><span data-stu-id="3c76f-125">This example uses the **Clone** method to create copies of a recordset and then lets the user position the record pointer of each copy independently.</span></span>

```vb
    Sub CloneX() 
     
       Dim dbsNorthwind As Database 
       Dim arstProducts(1 To 3) As Recordset2 
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
