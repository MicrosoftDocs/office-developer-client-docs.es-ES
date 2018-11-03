---
title: TableDef.CreateIndex (método) (DAO)
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
ms.openlocfilehash: 73b6fb5c5a4b0b91904c92a1b445ddc41cb7c73e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931347"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="8365c-102">TableDef.CreateIndex (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="8365c-102">TableDef.CreateIndex method (DAO)</span></span>


<span data-ttu-id="8365c-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8365c-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="8365c-p101">Crea un nuevo objeto **[Index](index-object-dao.md)** (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8365c-p101">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="8365c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8365c-106">Syntax</span></span>

<span data-ttu-id="8365c-107">*expresión* . CreateIndex (***nombre***)</span><span class="sxs-lookup"><span data-stu-id="8365c-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="8365c-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="8365c-108">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8365c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8365c-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8365c-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="8365c-110">Name</span></span></p></th>
<th><p><span data-ttu-id="8365c-111">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="8365c-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8365c-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8365c-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8365c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8365c-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8365c-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="8365c-114">Name</span></span></p></td>
<td><p><span data-ttu-id="8365c-115">Opcional</span><span class="sxs-lookup"><span data-stu-id="8365c-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="8365c-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8365c-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8365c-p102"><strong>String</strong> que identifica inequívocamente el nuevo objeto <strong>Index</strong>. Vea el tema relativo a la propiedad <strong>Name</strong> para obtener información detallada sobre los nombres de <strong>Index</strong> válidos.</span><span class="sxs-lookup"><span data-stu-id="8365c-p102">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object. See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8365c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8365c-119">Return value</span></span>

<span data-ttu-id="8365c-120">Index</span><span class="sxs-lookup"><span data-stu-id="8365c-120">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="8365c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8365c-121">Remarks</span></span>

<span data-ttu-id="8365c-122">Puede utilizar el método **CreateIndex** para crear un nuevo objeto **Index** para un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8365c-122">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="8365c-123">Si se omite la parte del nombre opcional cuando utiliza **CreateIndex**, puede usar una instrucción de asignación adecuada para establecer o restablecer la propiedad **Name** antes de agregar el nuevo objeto a una colección.</span><span class="sxs-lookup"><span data-stu-id="8365c-123">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="8365c-124">Después de agregar el objeto, podrá o no establecer su propiedad **Name** en función del tipo de objeto que contenga la colección **Indexes**.</span><span class="sxs-lookup"><span data-stu-id="8365c-124">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="8365c-125">Vea el tema correspondiente a la propiedad **Name** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8365c-125">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="8365c-126">Si name hace referencia a un objeto que ya es un miembro de la colección, se produce un error en tiempo de ejecución cuando se utiliza el método **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="8365c-126">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="8365c-127">Para quitar un objeto **Index** de una colección, utilice el método **[Delete](fields-delete-method-dao.md)** en la colección.</span><span class="sxs-lookup"><span data-stu-id="8365c-127">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="8365c-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8365c-128">Example</span></span>

<span data-ttu-id="8365c-p104">En este ejemplo se utiliza el método **CreateIndex** para crear dos objetos **Index** nuevos y agregarlos después a la colección **Indexes** del objeto **TableDef** de empleados. A continuación, se enumera la colección Indexes del objeto **TableDef**, la colección **Fields** de los nuevos objetos **Index** y la colección Properties de los nuevos objetos **Index**. Se requiere la función CreateIndexOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="8365c-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

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
