---
title: Propiedad Field2.AllowZeroLength (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: d3795634-527f-b4c5-b606-50f9945cac12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834791(v=office.15)
ms:contentKeyID: 48547908
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3125a5669ea8aa016d8554be0357572d56c08ecf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721181"
---
# <a name="field2allowzerolength-property-dao"></a><span data-ttu-id="a96df-102">Propiedad Field2.AllowZeroLength (DAO)</span><span class="sxs-lookup"><span data-stu-id="a96df-102">Field2.AllowZeroLength property (DAO)</span></span>


<span data-ttu-id="a96df-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a96df-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a96df-104">Establece o devuelve un valor que indica si una cadena de longitud cero ("") es válida para la propiedad **[Value](field-value-property-dao.md)** del objeto **Field2** con un tipo de datos Text o Memo (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a96df-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **Field2** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a96df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a96df-105">Syntax</span></span>

<span data-ttu-id="a96df-106">*expresión* . Permitir longitud cero</span><span class="sxs-lookup"><span data-stu-id="a96df-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="a96df-107">*expresión* Variable que representa un objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="a96df-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a96df-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a96df-108">Remarks</span></span>

<span data-ttu-id="a96df-109">Para un objeto que aún no se haya anexado a la colección **Fields**, esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a96df-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="a96df-110">Una vez que se haya anexado a una colección **Fields**, la disponibilidad de la propiedad **AllowZeroLength** depende del objeto que contiene la colección **Fields**, como se muestra en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a96df-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a96df-111">Si la colección Fields pertenece a</span><span class="sxs-lookup"><span data-stu-id="a96df-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="a96df-112">Disponibilidad de AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="a96df-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a96df-113">							Objeto <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a96df-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a96df-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="a96df-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96df-115">							Objeto <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a96df-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a96df-116">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a96df-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96df-117">							Objeto <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a96df-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a96df-118">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a96df-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a96df-119">							Objeto <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a96df-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a96df-120">No admitido</span><span class="sxs-lookup"><span data-stu-id="a96df-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a96df-121">							Objeto <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a96df-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a96df-122">Es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a96df-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a96df-123">Puede usar esta propiedad junto con la propiedad **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** o **[ValidationRule](field-validationrule-property-dao.md)** para validar un valor de un campo.</span><span class="sxs-lookup"><span data-stu-id="a96df-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="a96df-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a96df-124">Example</span></span>

<span data-ttu-id="a96df-p101">En este ejemplo, la propiedad **AllowZeroLength** permite al usuario establecer el valor de un objeto **Field2** en una cadena vacía. En esta situación, el usuario puede distinguir entre un registro en el que no se conocen los datos y un registro en el que los datos no son aplicables.</span><span class="sxs-lookup"><span data-stu-id="a96df-p101">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field2** to an empty string. In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
