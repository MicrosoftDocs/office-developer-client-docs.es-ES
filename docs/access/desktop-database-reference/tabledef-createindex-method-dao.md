---
title: Método TableDef.CreateIndex (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: baa82b659cc2260d4a003c644b2d03d6c897fd21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314374"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="942a7-102">Método TableDef.CreateIndex (DAO)</span><span class="sxs-lookup"><span data-stu-id="942a7-102">TableDef.CreateIndex method (DAO)</span></span>

<span data-ttu-id="942a7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="942a7-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="942a7-p101">Crea un nuevo objeto **[Index](index-object-dao.md)** (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="942a7-p101">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="942a7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="942a7-106">Syntax</span></span>

<span data-ttu-id="942a7-107">*expresión* . CreateIndex(***Name***)</span><span class="sxs-lookup"><span data-stu-id="942a7-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="942a7-108">*expression* Variable que representa un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="942a7-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="942a7-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="942a7-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="942a7-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="942a7-110">Name</span></span></p></th>
<th><p><span data-ttu-id="942a7-111">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="942a7-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="942a7-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="942a7-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="942a7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="942a7-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="942a7-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="942a7-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="942a7-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="942a7-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="942a7-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="942a7-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="942a7-p102"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Index</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Index</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="942a7-p102">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object. See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="942a7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="942a7-119">Return value</span></span>

<span data-ttu-id="942a7-120">Índice</span><span class="sxs-lookup"><span data-stu-id="942a7-120">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="942a7-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="942a7-121">Remarks</span></span>

<span data-ttu-id="942a7-p103">Puede utilizar el método **CreateIndex** para crear un nuevo objeto **Index** para un objeto **TableDef**. Si omite el argumento name opcional cuando utiliza **CreateIndex**, puede usar la instrucción de asignación pertinente para establecer o restablecer la propiedad **Name** antes de agregar el nuevo objeto a la colección. Después de agregar el objeto, podrá o no establecer su propiedad **Name** en función del tipo de objeto que contenga la colección **Indexes**. Vea el tema correspondiente a la propiedad **Name** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="942a7-p103">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object. If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection. After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection. See the **Name** property topic for more details.</span></span>

<span data-ttu-id="942a7-126">Si name hace referencia a un objeto que ya es miembro de la colección, se produce un error en tiempo de ejecución cuando se usa el **[método Append.](fields-append-method-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="942a7-126">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="942a7-127">Para quitar un objeto **Index** de una colección, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección.</span><span class="sxs-lookup"><span data-stu-id="942a7-127">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="942a7-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="942a7-128">Example</span></span>

<span data-ttu-id="942a7-p104">En este ejemplo se utiliza el método **CreateIndex** para crear dos objetos **Index** nuevos y agregarlos después a la colección **Indexes** del objeto **TableDef** de empleados. A continuación, se enumera la colección Indexes del objeto **TableDef**, la colección **Fields** de los nuevos objetos **Index** y la colección Properties de los nuevos objetos **Index**. Se requiere la función CreateIndexOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="942a7-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
