---
title: Propiedad Field2.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 26d37bfda90f2ab4e2627b936d3cf37b5be811d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726333"
---
# <a name="field2ordinalposition-property-dao"></a><span data-ttu-id="8e9ce-102">Propiedad Field2.OrdinalPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="8e9ce-102">Field2.OrdinalPosition property (DAO)</span></span>


<span data-ttu-id="8e9ce-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e9ce-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8e9ce-p101">Establece o devuelve la posición relativa de un objeto **Field2** en una colección **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-p101">Sets or returns the relative position of a **Field2** object within a **[Fields](fields-collection-dao.md)** collection. .</span></span>

## <a name="syntax"></a><span data-ttu-id="8e9ce-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e9ce-106">Syntax</span></span>

<span data-ttu-id="8e9ce-107">*expresión* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="8e9ce-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="8e9ce-108">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="8e9ce-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e9ce-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e9ce-109">Remarks</span></span>

<span data-ttu-id="8e9ce-110">Para un objeto que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="8e9ce-111">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-111">The default is 0.</span></span>

<span data-ttu-id="8e9ce-112">La disponibilidad de la propiedad **OrdinalPosition** depende del objeto que contiene la colección **Fields**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e9ce-113">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="8e9ce-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="8e9ce-114">
Entonces OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="8e9ce-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e9ce-115">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="8e9ce-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e9ce-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="8e9ce-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e9ce-117">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="8e9ce-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e9ce-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e9ce-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e9ce-119">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="8e9ce-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e9ce-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e9ce-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e9ce-121">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="8e9ce-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e9ce-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="8e9ce-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e9ce-123">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="8e9ce-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8e9ce-124">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e9ce-p102">Generalmente, la posición ordinal de un objeto anexado a una colección depende del orden en el que se anexe el objeto. El primer objeto anexado estará en la primera posición (0), el segundo estará en la segunda posición (1) y así sucesivamente. El último objeto anexado estará en la posición ordinal recuento – 1, donde recuento es el número de objetos en la colección tal y como aparece especificado en el valor de la propiedad **[Count](containers-count-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-p102">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object. The first appended object is in the first position (0), the second appended object is in the second position (1), and so on. The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="8e9ce-128">Puede utilizar la propiedad **OrdinalPosition** para especificar una posición ordinal para los nuevos objetos **Field2** que difiera del orden en el que ha anexado esos objetos a una colección.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field2** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="8e9ce-129">Esto permite especificar un orden de campo para sus tablas, consultas y conjuntos de registros cuando los utiliza en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="8e9ce-130">Por ejemplo, el orden en el que los campos se devuelven en una instrucción SELECT \* consulta viene determinada por los valores de propiedad **OrdinalPosition** actuales.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="8e9ce-131">Puede restablecer permanentemente el orden en el que los campos se devuelven en los conjuntos de registros estableciendo la propiedad **OrdinalPosition** en cualquier entero positivo.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="8e9ce-p104">Dos o más objetos **Field2** en la misma colección pueden tener el mismo valor que la propiedad **OrdinalPosition**, en cuyo caso se ordenarán alfabéticamente. Por ejemplo, si tiene un campo denominado Edad establecido en 4 y establece un segundo campo denominado Peso en 4, Peso se devuelve después de Edad.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-p104">Two or more **Field2** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="8e9ce-p105">Puede especificar un número que sea mayor que el número de campos menos 1. El campo se devolverá siguiendo un orden respecto al número más grande. Por ejemplo, si establece una propiedad de campo **OrdinalPosition** en 20 (y sólo hay 5 campos) y ha establecido la propiedad **OrdinalPosition** para dos campos más en 10 y en 30, respectivamente, el campo establecido en 20 se devolverá entre los campos establecidos en 10 y en 30.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>


> [!NOTE]
> <span data-ttu-id="8e9ce-137">Incluso si no se ha actualizado la colección **Fields** de un objeto **[TableDef](tabledef-object-dao.md)** , el orden de los campos en un **[objeto Recordset](recordset-object-dao.md)** abierto desde **TableDef** reflejará los datos de **OrdinalPosition** del objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="8e9ce-137">Even if the **Fields** collection of a **[TableDef](tabledef-object-dao.md)** object has not been refreshed, the field order in a **[Recordset](recordset-object-dao.md)** opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object.</span></span> <span data-ttu-id="8e9ce-138">Un tipo de tabla **Recordset** tendrá los mismos datos **OrdinalPosition** que la tabla base, pero cualquier otro tipo de **Recordset** tendrá nuevos datos **OrdinalPosition** (comenzando por 0) que sigue el orden determinado por los datos de **OrdinalPosition** del objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-138">A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span></span>



## <a name="example"></a><span data-ttu-id="8e9ce-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8e9ce-139">Example</span></span>

<span data-ttu-id="8e9ce-p107">En este ejemplo se cambian los valores de la propiedad **OrdinalPosition** para Employees **TableDef** de forma que se controla el orden de **Field2** en un resultado **Recordset**. Al establecer la **OrdinalPosition** de todos los **Fields** en 1, cualquier **Recordset** resultante ordenará los **Fields** alfabéticamente. Observe que los valores **OrdinalPosition** en **Recordset** no coinciden con los valores de **TableDef**, pero solo reflejan el resultado final de los cambios de **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8e9ce-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field2** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
