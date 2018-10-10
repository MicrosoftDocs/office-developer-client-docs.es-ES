---
title: Field2.OrdinalPosition Property (DAO)
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
ms.openlocfilehash: 5c086263ffe2267a8f01cfae2e67db125313c0b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484010"
---
# <a name="field2ordinalposition-property-dao"></a><span data-ttu-id="a49a8-102">Field2.OrdinalPosition Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="a49a8-102">Field2.OrdinalPosition Property (DAO)</span></span>


<span data-ttu-id="a49a8-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a49a8-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a49a8-p101">Establece o devuelve la posición relativa de un objeto **Field2** en una colección **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="a49a8-p101">Sets or returns the relative position of a **Field2** object within a **[Fields](fields-collection-dao.md)** collection. .</span></span>

## <a name="syntax"></a><span data-ttu-id="a49a8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a49a8-106">Syntax</span></span>

<span data-ttu-id="a49a8-107">*expresión* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="a49a8-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="a49a8-108">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="a49a8-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a49a8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a49a8-109">Remarks</span></span>

<span data-ttu-id="a49a8-110">Para un objeto que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a49a8-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="a49a8-111">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="a49a8-111">The default is 0.</span></span>

<span data-ttu-id="a49a8-112">La disponibilidad de la propiedad **OrdinalPosition** depende del objeto que contiene la colección **Fields**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a49a8-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a49a8-113">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="a49a8-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="a49a8-114">
Entonces OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="a49a8-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a49a8-115">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a49a8-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a49a8-116">No admitido</span><span class="sxs-lookup"><span data-stu-id="a49a8-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a49a8-117">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a49a8-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a49a8-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a49a8-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a49a8-119">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a49a8-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a49a8-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a49a8-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a49a8-121">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a49a8-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a49a8-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="a49a8-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a49a8-123">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a49a8-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a49a8-124">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a49a8-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a49a8-p102">Generalmente, la posición ordinal de un objeto anexado a una colección depende del orden en el que se anexe el objeto. El primer objeto anexado estará en la primera posición (0), el segundo estará en la segunda posición (1) y así sucesivamente. El último objeto anexado estará en la posición ordinal recuento – 1, donde recuento es el número de objetos en la colección tal y como aparece especificado en el valor de la propiedad **[Count](containers-count-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="a49a8-p102">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object. The first appended object is in the first position (0), the second appended object is in the second position (1), and so on. The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="a49a8-128">Puede utilizar la propiedad **OrdinalPosition** para especificar una posición ordinal para los nuevos objetos **Field2** que difiera del orden en el que ha anexado esos objetos a una colección.</span><span class="sxs-lookup"><span data-stu-id="a49a8-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field2** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="a49a8-129">Esto permite especificar un orden de campo para sus tablas, consultas y conjuntos de registros cuando los utiliza en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="a49a8-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="a49a8-130">Por ejemplo, el orden en el que los campos se devuelven en una instrucción SELECT \* consulta viene determinada por los valores de propiedad **OrdinalPosition** actuales.</span><span class="sxs-lookup"><span data-stu-id="a49a8-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="a49a8-131">Puede restablecer permanentemente el orden en el que los campos se devuelven en los conjuntos de registros estableciendo la propiedad **OrdinalPosition** en cualquier entero positivo.</span><span class="sxs-lookup"><span data-stu-id="a49a8-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="a49a8-p104">Dos o más objetos **Field2** en la misma colección pueden tener el mismo valor que la propiedad **OrdinalPosition**, en cuyo caso se ordenarán alfabéticamente. Por ejemplo, si tiene un campo denominado Edad establecido en 4 y establece un segundo campo denominado Peso en 4, Peso se devuelve después de Edad.</span><span class="sxs-lookup"><span data-stu-id="a49a8-p104">Two or more **Field2** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="a49a8-p105">Puede especificar un número que sea mayor que el número de campos menos 1. El campo se devolverá siguiendo un orden respecto al número más grande. Por ejemplo, si establece una propiedad de campo **OrdinalPosition** en 20 (y sólo hay 5 campos) y ha establecido la propiedad **OrdinalPosition** para dos campos más en 10 y en 30, respectivamente, el campo establecido en 20 se devolverá entre los campos establecidos en 10 y en 30.</span><span class="sxs-lookup"><span data-stu-id="a49a8-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a49a8-p106">[!NOTA] Incluso si la colección <STRONG>Fields</STRONG> de un <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> no se actualizó, el orden del campo en un <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> abierto desde <STRONG>TableDef</STRONG> reflejará los datos de <STRONG>OrdinalPosition</STRONG> del objeto <STRONG>TableDef</STRONG>. Un tipo de tabla <STRONG>Recordset</STRONG> tendrá los mismos datos <STRONG>OrdinalPosition</STRONG> que la tabla base, pero cualquier otro tipo de <STRONG>Recordset</STRONG> tendrá nuevos datos <STRONG>OrdinalPosition</STRONG> (comenzando por 0) que sigue el orden determinado por los datos de <STRONG>OrdinalPosition</STRONG> del objeto <STRONG>TableDef</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="a49a8-p106">Even if the <STRONG>Fields</STRONG> collection of a <STRONG><A href="tabledef-object-dao.md">TableDef</A></STRONG> has not been refreshed, the field order in a <STRONG><A href="recordset-object-dao.md">Recordset</A></STRONG> opened from the <STRONG>TableDef</STRONG> will reflect the <STRONG>OrdinalPosition</STRONG> data of the <STRONG>TableDef</STRONG> object. A table-type <STRONG>Recordset</STRONG> will have the same <STRONG>OrdinalPosition</STRONG> data as the underlying table, but any other type of <STRONG>Recordset</STRONG> will have new <STRONG>OrdinalPosition</STRONG> data (starting with 0) that follow the order determined by the <STRONG>OrdinalPosition</STRONG> data of the <STRONG>TableDef</STRONG>.</span></span></P>



## <a name="example"></a><span data-ttu-id="a49a8-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a49a8-139">Example</span></span>

<span data-ttu-id="a49a8-p107">En este ejemplo se cambian los valores de la propiedad **OrdinalPosition** para Employees **TableDef** de forma que se controla el orden de **Field2** en un resultado **Recordset**. Al establecer la **OrdinalPosition** de todos los **Fields** en 1, cualquier **Recordset** resultante ordenará los **Fields** alfabéticamente. Observe que los valores **OrdinalPosition** en **Recordset** no coinciden con los valores de **TableDef**, pero solo reflejan el resultado final de los cambios de **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="a49a8-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field2** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

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