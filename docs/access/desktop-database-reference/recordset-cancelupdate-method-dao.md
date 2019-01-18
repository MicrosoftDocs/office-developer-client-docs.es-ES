---
title: Recordset.CancelUpdate (método) (DAO)
TOCTitle: CancelUpdate method
ms:assetid: efc4f60b-876f-5e11-37fd-0fbbf225b15b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836421(v=office.15)
ms:contentKeyID: 48548590
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053072
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5950154d8896678889af01254104a2ac0dfef4cc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712438"
---
# <a name="recordsetcancelupdate-method-dao"></a><span data-ttu-id="b0f9a-102">Recordset.CancelUpdate (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="b0f9a-102">Recordset.CancelUpdate method (DAO)</span></span>

<span data-ttu-id="b0f9a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0f9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0f9a-104">Cancela todas las actualizaciones pendientes para un objeto **[Recordset](recordset-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-104">Cancels any pending updates for a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f9a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0f9a-105">Syntax</span></span>

<span data-ttu-id="b0f9a-106">*expresión* . CancelUpdate (***UpdateType***)</span><span class="sxs-lookup"><span data-stu-id="b0f9a-106">*expression* .CancelUpdate(***UpdateType***)</span></span>

<span data-ttu-id="b0f9a-107">*expresión* Variable que representa un objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b0f9a-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0f9a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0f9a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0f9a-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="b0f9a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b0f9a-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="b0f9a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b0f9a-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b0f9a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="b0f9a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0f9a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0f9a-113"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="b0f9a-113"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="b0f9a-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="b0f9a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b0f9a-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="b0f9a-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="b0f9a-116">Establecer en uno de los valores <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="b0f9a-116">Set to one of the <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> values.</span></span></p><p><span data-ttu-id="b0f9a-117"><strong>Nota</strong>: los valores de <EM>valores dbUpdateRegular</EM> y <EM>dbUpdateBatch</EM> son válidos sólo si está habilitada la actualización por lotes.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-117"><strong>NOTE</strong>: The <EM>dbUpdateRegular</EM> and <EM>dbUpdateBatch</EM> values are valid only if batch updating is enabled.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b0f9a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0f9a-118">Remarks</span></span>

<span data-ttu-id="b0f9a-p101">Puede utilizar el método **CancelUpdate** para cancelar todas las operaciones pendientes resultantes de una operación **[Edit](recordset-edit-method-dao.md)** o **[AddNew](recordset-addnew-method-dao.md)**. Por ejemplo, si un usuario llama al método **Edit** o **AddNew** y aún no se ha invocado el método **Update**, **CancelUpdate** cancela todos los cambios efectuados después de la llamada a **Edit** o **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-p101">You can use the **CancelUpdate** method to cancel any pending updates resulting from an **[Edit](recordset-edit-method-dao.md)** or **[AddNew](recordset-addnew-method-dao.md)** operation. For example, if a user invokes the **Edit** or **AddNew** method and hasn't yet invoked the **Update** method, **CancelUpdate** cancels any changes made after **Edit** or **AddNew** was invoked.</span></span>

<span data-ttu-id="b0f9a-121">Compruebe la propiedad **[EditMode](recordset-editmode-property-dao.md)** del objeto **Recordset** para determinar si hay alguna operación pendiente que se pueda cancelar.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-121">Check the **[EditMode](recordset-editmode-property-dao.md)** property of the **Recordset** to determine if there is a pending operation that can be canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="b0f9a-122">[!NOTA] El método **CancelUpdate** tiene el mismo efecto que desplazarse a otro registro sin usar el método **[Update](recordset-update-method-dao.md)**, con la diferencia de que el registro actual no cambia y algunas propiedades, como **[BOF](recordset-bof-property-dao.md)** y **[EOF](recordset-eof-property-dao.md)** no se actualizan.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-122">Using the **CancelUpdate** method has the same effect as moving to another record without using the **[Update](recordset-update-method-dao.md)** method, except that the current record doesn't change, and various properties, such as **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)**, aren't updated.</span></span>


## <a name="example"></a><span data-ttu-id="b0f9a-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b0f9a-123">Example</span></span>

<span data-ttu-id="b0f9a-124">En este ejemplo se muestra cómo se utiliza el método **CancelUpdate** con el método **AddNew**.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-124">This example shows how the **CancelUpdate** method is used with the **AddNew** method.</span></span>

```vb
    Sub CancelUpdateX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim intCommand As Integer 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
          "Employees", dbOpenDynaset) 
     
       With rstEmployees 
          .AddNew 
          !FirstName = "Kimberly" 
          !LastName = "Bowen" 
          intCommand = MsgBox("Add new record for " & _ 
             !FirstName & " " & !LastName & "?", vbYesNo) 
          If intCommand = vbYes Then 
             .Update 
             MsgBox "Record added." 
             ' Delete new record because this is a  
             ' demonstration. 
             .Bookmark = .LastModified 
             .Delete 
          Else 
             .CancelUpdate 
             MsgBox "Record not added." 
          End If 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="b0f9a-125">En este ejemplo se muestra cómo se utiliza el método **CancelUpdate** con el método **Edit**.</span><span class="sxs-lookup"><span data-stu-id="b0f9a-125">This example shows how the **CancelUpdate** method is used with the **Edit** method.</span></span>

```vb
Sub CancelUpdateX2() 
 
   Dim dbsNorthwind As Database 
   Dim rstEmployees As Recordset 
   Dim strFirst As String 
   Dim strLast As String 
   Dim intCommand As Integer 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
   Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
      "Employees", dbOpenDynaset) 
 
   With rstEmployees 
      strFirst = !FirstName 
      strLast = !LastName 
      .Edit 
      !FirstName = "Cora" 
      !LastName = "Edmonds" 
      intCommand = MsgBox("Replace current name with " & _ 
         !FirstName & " " & !LastName & "?", vbYesNo) 
      If intCommand = vbYes Then 
         .Update 
         MsgBox "Record modified." 
         ' Restore data because this is a demonstration. 
         .Bookmark = .LastModified 
         .Edit 
         !FirstName = strFirst 
         !LastName = strLast 
         .Update 
      Else 
         .CancelUpdate 
         MsgBox "Record not modified." 
      End If 
      .Close 
   End With 
 
   dbsNorthwind.Close 
 
End Sub 
 
```

