---
title: Field2.Required Property (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 048c4dc46f03af213dee090b839dfcc67d4f48ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485899"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="0551e-102">Field2.Required Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="0551e-102">Field2.Required Property (DAO)</span></span>


<span data-ttu-id="0551e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0551e-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="0551e-104">Establece o devuelve un valor que indica si un objeto **Field2** requiere un valor no Null.</span><span class="sxs-lookup"><span data-stu-id="0551e-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0551e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0551e-105">Syntax</span></span>

<span data-ttu-id="0551e-106">*expresión* . Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0551e-106">*expression* .Required</span></span>

<span data-ttu-id="0551e-107">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="0551e-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0551e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0551e-108">Remarks</span></span>

<span data-ttu-id="0551e-109">Para un **Field2** que no está todavía anexado a la colección **Fields**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0551e-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="0551e-110">La disponibilidad de la propiedad **Required** depende del objeto que contiene la colección **[Fields](fields-collection-dao.md)**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="0551e-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0551e-111">Si la colección Fields pertenece a un</span><span class="sxs-lookup"><span data-stu-id="0551e-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="0551e-112">Entonces Required</span><span class="sxs-lookup"><span data-stu-id="0551e-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0551e-113">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="0551e-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0551e-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="0551e-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0551e-115">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="0551e-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0551e-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0551e-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0551e-117">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="0551e-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0551e-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="0551e-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0551e-119">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="0551e-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0551e-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="0551e-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0551e-121">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="0551e-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="0551e-122">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0551e-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0551e-p101">Puede utilizar la propiedad **Required** junto con la propiedad **AllowZeroLength**, **ValidateOnSet** o **ValidationRule** para determinar la validez del valor de la propiedad **Value** para ese objeto **Field2**. Si la propiedad **Required** está establecida como **False**, el campo puede contener valores **null**, así como valores que cumplan las condiciones especificadas por los valores de las propiedades **AllowZeroLength** y **ValidationRule**.</span><span class="sxs-lookup"><span data-stu-id="0551e-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0551e-p102">[!NOTA] Cuando pueda establecer esta propiedad tanto para un objeto <STRONG>Index</STRONG> como para un objeto <STRONG>Field2</STRONG>, establézcala para el objeto <STRONG>Field2</STRONG>. La validez del valor de la propiedad para un objeto <STRONG>Field2</STRONG> se comprueba antes que para un objeto <STRONG>Index</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="0551e-p102">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field2</STRONG> object, set it for the <STRONG>Field2</STRONG> object. The validity of the property setting for a <STRONG>Field2</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="0551e-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0551e-127">Example</span></span>

<span data-ttu-id="0551e-p103">En este ejemplo se utiliza la propiedad **Required** que informa sobre qué campo de tres tablas distintas debe contener los datos necesarios para agregar un nuevo registro. El procedimiento RequiredOutput es necesario para ejecutar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="0551e-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```
