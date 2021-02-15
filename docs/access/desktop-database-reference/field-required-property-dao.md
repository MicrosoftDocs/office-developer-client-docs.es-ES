---
title: Propiedad Field.Required (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 52900d4a60002695866b9960fb6b80cefeb2b2ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292982"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="18284-102">Propiedad Field.Required (DAO)</span><span class="sxs-lookup"><span data-stu-id="18284-102">Field.Required property (DAO)</span></span>


<span data-ttu-id="18284-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18284-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18284-104">Establece o devuelve un valor que indica si un objeto **[Field](field-object-dao.md)** requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="18284-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="18284-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18284-105">Syntax</span></span>

<span data-ttu-id="18284-106">*expresión* . Obligatorio</span><span class="sxs-lookup"><span data-stu-id="18284-106">*expression* .Required</span></span>

<span data-ttu-id="18284-107">*expression* Variable que representa un objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="18284-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="18284-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="18284-108">Remarks</span></span>

<span data-ttu-id="18284-109">Para un **Field** que todavía no está anexado a la colección **Fields**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="18284-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="18284-110">La disponibilidad de la propiedad **Required** depende del objeto que contiene la colección [Fields](fields-collection-dao.md), como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="18284-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18284-111">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="18284-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="18284-112">Entonces Required</span><span class="sxs-lookup"><span data-stu-id="18284-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18284-113">
						Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="18284-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="18284-114">No está admitido</span><span class="sxs-lookup"><span data-stu-id="18284-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18284-115">
						Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="18284-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="18284-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="18284-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18284-117">
						Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="18284-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="18284-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="18284-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18284-119">
						Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="18284-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="18284-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="18284-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18284-121">
						Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="18284-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="18284-122">Lectura y escritura</span><span class="sxs-lookup"><span data-stu-id="18284-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="18284-p101">Puede utilizar la propiedad **Required** junto con la propiedad **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** o **[ValidationRule](field-validationrule-property-dao.md)** para determinar la validez del valor de la propiedad **[Value](field-value-property-dao.md)** para ese objeto **Field**. Si la propiedad **Required** está establecida en **False**, el campo puede contener valores **null**, así como valores que cumplan las condiciones especificadas por los valores de las propiedades **AllowZeroLength** y **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="18284-p101">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="18284-p102">[!NOTA] Cuando pueda establecer esta propiedad tanto para un objeto **Index** como para un objeto **Field**, establézcala para el objeto **Field**. La validez del valor de la propiedad para un objeto **Field** se comprueba antes que para un objeto **Index**.</span><span class="sxs-lookup"><span data-stu-id="18284-p102">When you can set this property for either an **Index** object or a **Field** object, set it for the **Field** object. The validity of the property setting for a **Field** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="18284-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="18284-127">Example</span></span>

<span data-ttu-id="18284-p103">En este ejemplo se utiliza la propiedad **Required** que informa sobre qué campo de tres tablas distintas debe contener los datos necesarios para agregar un nuevo registro. El procedimiento RequiredOutput es necesario para ejecutar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="18284-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

