---
title: TableDef.CreateIndex Method (DAO)
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
ms.openlocfilehash: 1c0dd3a48274c7a0affae9caa87ec762bea498ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606377"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="97f49-102">TableDef.CreateIndex Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="97f49-102">TableDef.CreateIndex Method (DAO)</span></span>


<span data-ttu-id="97f49-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="97f49-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="97f49-p101">Crea un nuevo objeto **[Index](index-object-dao.md)** (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="97f49-p101">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="97f49-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97f49-106">Syntax</span></span>

<span data-ttu-id="97f49-107">*expresión* . CreateIndex (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="97f49-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="97f49-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="97f49-108">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="97f49-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97f49-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97f49-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="97f49-110">Name</span></span></p></th>
<th><p><span data-ttu-id="97f49-111">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="97f49-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="97f49-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="97f49-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="97f49-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="97f49-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97f49-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="97f49-114">Name</span></span></p></td>
<td><p><span data-ttu-id="97f49-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="97f49-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="97f49-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="97f49-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="97f49-p102"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Index</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Index</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="97f49-p102">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object. See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="97f49-119"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="97f49-119"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="97f49-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97f49-120">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="97f49-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97f49-121">Return value</span></span>
>>>>>>> <span data-ttu-id="97f49-122">master</span><span class="sxs-lookup"><span data-stu-id="97f49-122">master</span></span>

<span data-ttu-id="97f49-123">Index</span><span class="sxs-lookup"><span data-stu-id="97f49-123">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="97f49-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97f49-124">Remarks</span></span>

<span data-ttu-id="97f49-125">Puede utilizar el método **CreateIndex** para crear un nuevo objeto **Index** para un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="97f49-125">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="97f49-126">Si se omite la parte del nombre opcional cuando utiliza **CreateIndex**, puede usar una instrucción de asignación adecuada para establecer o restablecer la propiedad **Name** antes de agregar el nuevo objeto a una colección.</span><span class="sxs-lookup"><span data-stu-id="97f49-126">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="97f49-127">Después de agregar el objeto, podrá o no establecer su propiedad **Name** en función del tipo de objeto que contenga la colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="97f49-127">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="97f49-128">Vea el tema correspondiente a la propiedad **Name** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="97f49-128">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="97f49-129">Si name hace referencia a un objeto que ya es un miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="97f49-129">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="97f49-130">Para quitar un objeto **Index** de una colección, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección.</span><span class="sxs-lookup"><span data-stu-id="97f49-130">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="97f49-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97f49-131">Example</span></span>

<span data-ttu-id="97f49-p104">En este ejemplo se utiliza el método **CreateIndex** para crear dos objetos **Index** nuevos y agregarlos después a la colección **Indexes** del objeto **TableDef** de empleados. A continuación, se enumera la colección Indexes del objeto **TableDef**, la colección **Fields** de los nuevos objetos **Index** y la colección Properties de los nuevos objetos **Index**. Se requiere la función CreateIndexOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="97f49-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

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
