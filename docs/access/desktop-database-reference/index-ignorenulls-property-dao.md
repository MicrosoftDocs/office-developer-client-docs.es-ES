---
title: Index.IgnoreNulls Property (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b6c190b7a61e26ff6e4abedc1a19bde26a1de426
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485192"
---
# <a name="indexignorenulls-property-dao"></a><span data-ttu-id="84f1e-102">Index.IgnoreNulls Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="84f1e-102">Index.IgnoreNulls Property (DAO)</span></span>


<span data-ttu-id="84f1e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="84f1e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="84f1e-104">Establece o devuelve un valor que indica si los registros con valores Null en sus campos de índice tienen entradas de índice (sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="84f1e-104">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="84f1e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84f1e-105">Syntax</span></span>

<span data-ttu-id="84f1e-106">*expresión* . IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="84f1e-106">*expression* .IgnoreNulls</span></span>

<span data-ttu-id="84f1e-107">*expresión* Variable que representa un objeto **Index** .</span><span class="sxs-lookup"><span data-stu-id="84f1e-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f1e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84f1e-108">Remarks</span></span>

<span data-ttu-id="84f1e-109">Esta propiedad es de lectura y escritura para un nuevo objeto **[Index](index-object-dao.md)** que todavía no está anexado a una colección y es de solo lectura para un objeto **Index** existente en una colección **[Indexes](indexes-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="84f1e-109">This property is read/write for a new **[Index](index-object-dao.md)** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span>

<span data-ttu-id="84f1e-p101">Para acelerar el proceso de búsqueda de registros, puede definir un índice para un campo. Si permite entradas **null** en un campo indizado y espera que muchas de las entradas sean **null**, puede establecer la propiedad **IgnoreNulls** para el objeto **Index** en **True** para reducir la cantidad de espacio de almacenamiento que usa el índice.</span><span class="sxs-lookup"><span data-stu-id="84f1e-p101">To speed up the process of searching for records, you can define an index for a field. If you allow **null** entries in an indexed field and expect many of the entries to be **null**, you can set the **IgnoreNulls** property for the **Index** object to **True** to reduce the amount of storage space that the index uses.</span></span>

<span data-ttu-id="84f1e-112">El valor de la propiedad **IgnoreNulls** y el valor de la propiedad **[Required](field-required-property-dao.md)** determinan juntos si un registro con un valor de índice **null** tiene una entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="84f1e-112">The **IgnoreNulls** property setting and the **[Required](field-required-property-dao.md)** property setting together determine whether a record with a **null** index value has an index entry.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84f1e-113">Si IgnoreNulls es</span><span class="sxs-lookup"><span data-stu-id="84f1e-113">If IgnoreNulls is</span></span></p></th>
<th><p><span data-ttu-id="84f1e-114">Y Required es</span><span class="sxs-lookup"><span data-stu-id="84f1e-114">And Required is</span></span></p></th>
<th><p><span data-ttu-id="84f1e-115">Entonces</span><span class="sxs-lookup"><span data-stu-id="84f1e-115">Then</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84f1e-116">True</span><span class="sxs-lookup"><span data-stu-id="84f1e-116">True</span></span></p></td>
<td><p><span data-ttu-id="84f1e-117">False</span><span class="sxs-lookup"><span data-stu-id="84f1e-117">False</span></span></p></td>
<td><p><span data-ttu-id="84f1e-118">Se permite un valor nulo en el campo de índice; no se agregó entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="84f1e-118">A null value is allowed in the index field; no index entry added.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84f1e-119">False</span><span class="sxs-lookup"><span data-stu-id="84f1e-119">False</span></span></p></td>
<td><p><span data-ttu-id="84f1e-120">False</span><span class="sxs-lookup"><span data-stu-id="84f1e-120">False</span></span></p></td>
<td><p><span data-ttu-id="84f1e-121">Se permite un valor nulo en el campo de índice; se agregó entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="84f1e-121">A null value is allowed in the index field; index entry added.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84f1e-122">True o False</span><span class="sxs-lookup"><span data-stu-id="84f1e-122">True or False</span></span></p></td>
<td><p><span data-ttu-id="84f1e-123">True</span><span class="sxs-lookup"><span data-stu-id="84f1e-123">True</span></span></p></td>
<td><p><span data-ttu-id="84f1e-124">No se permite un valor nulo en el campo de índice; no se agregó entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="84f1e-124">A null value isn't allowed in the index field; no index entry added.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="84f1e-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f1e-125">Example</span></span>

<span data-ttu-id="84f1e-126">En este ejemplo se establece la propiedad **IgnoreNulls** de un nuevo objeto **Index** en **True** o **False** a partir de los datos definidos por el usuario y después se demuestra el efecto en un objeto **Recordset** con un registro cuyo campo clave contiene un valor **Null**.</span><span class="sxs-lookup"><span data-stu-id="84f1e-126">This example sets the **IgnoreNulls** property of a new **Index** to **True** or **False** based on user input, and then demonstrates the effect on a **Recordset** with a record whose key field contains a **Null** value.</span></span>

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```