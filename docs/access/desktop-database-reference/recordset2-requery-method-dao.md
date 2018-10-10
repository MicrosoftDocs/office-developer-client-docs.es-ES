---
title: Recordset2.Requery Method (DAO)
TOCTitle: Requery Method
ms:assetid: d063c1e0-2fb7-b5cf-4d98-6f77a5a13cec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834712(v=office.15)
ms:contentKeyID: 48547837
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052940
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7019b0e4d3ffa916aea8436db14f3a8476f2e36f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483394"
---
# <a name="recordset2requery-method-dao"></a><span data-ttu-id="c4a8b-102">Recordset2.Requery Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="c4a8b-102">Recordset2.Requery Method (DAO)</span></span>


<span data-ttu-id="c4a8b-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4a8b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4a8b-104">Actualiza los datos de un objeto **[Recordset](recordset-object-dao.md)** volviendo a ejecutar la consulta en la que se basa el objeto.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a8b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4a8b-105">Syntax</span></span>

<span data-ttu-id="c4a8b-106">*expresión* . Requery (***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="c4a8b-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="c4a8b-107">*expresión* Variable que representa un objeto **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="c4a8b-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c4a8b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4a8b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4a8b-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="c4a8b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c4a8b-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="c4a8b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c4a8b-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c4a8b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c4a8b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4a8b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4a8b-113">NewQueryDef</span><span class="sxs-lookup"><span data-stu-id="c4a8b-113">NewQueryDef</span></span></p></td>
<td><p><span data-ttu-id="c4a8b-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="c4a8b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="c4a8b-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c4a8b-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c4a8b-116">Representa el valor de la propiedad <strong>Name</strong> de un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c4a8b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4a8b-117">Remarks</span></span>

<span data-ttu-id="c4a8b-118">Use este método para asegurarse de que un objeto **Recordset** contiene los datos más recientes.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="c4a8b-119">Este método rellena el actual **objeto Recordset** mediante el uso de los parámetros de consulta actuales o (en un área de trabajo de Microsoft Access) los nuevos proporcionados por el argumento newquerydef.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the newquerydef argument.</span></span>

<span data-ttu-id="c4a8b-120">Si no especifica un argumento newquerydef, el **objeto Recordset** se rellena volver a según la misma definición de consulta y los parámetros que se utilizaron originalmente para llenar el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-120">If you don't specify a newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="c4a8b-121">Cualquier cambio en los datos subyacentes se reflejará durante este nuevo relleno.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="c4a8b-122">Si no usó **QueryDef** para crear **Recordset**, **Recordset** se vuelve a crear desde cero.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="c4a8b-123">Si especifica **QueryDef** original en el argumento newquerydef, a continuación, se vuelve a consultar el **conjunto de registros** mediante los parámetros especificados por **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-123">If you specify the original **QueryDef** in the newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="c4a8b-124">Cualquier cambio en los datos subyacentes se reflejará durante este nuevo relleno.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="c4a8b-125">Para reflejar los cambios realizados en los valores de parámetro de consulta en el **conjunto de registros**, debe proporcionar el argumento newquerydef.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the newquerydef argument.</span></span>

<span data-ttu-id="c4a8b-126">Si especifica un objeto **QueryDef** diferente al que se usó originalmente para crear **Recordset**, **Recordset** se vuelve a crear desde cero.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="c4a8b-127">Cuando usa **Requery**, el primer registro de **Recordset** se convierte en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="c4a8b-128">No puede usar el método **Requery** en objetos **Recordset** de tipo dynaset o snapshot cuya propiedad **[Restartable](recordset2-restartable-property-dao.md)** está establecida en **False**.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset2-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="c4a8b-129">Sin embargo, si se proporciona el argumento opcional newquerydef, se omite la propiedad **Restartable** .</span><span class="sxs-lookup"><span data-stu-id="c4a8b-129">However, if you supply the optional newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="c4a8b-130">Si los dos valores de las propiedades **[BOF](recordset2-bof-property-dao.md)** y **[EOF](recordset2-eof-property-dao.md)** del objeto **Recordset** son **True** después de usar el método **Requery**, la consulta no devuelve ningún registro y **Recordset** no contiene datos.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-130">If both the **[BOF](recordset2-bof-property-dao.md)** and **[EOF](recordset2-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="c4a8b-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4a8b-131">Example</span></span>

<span data-ttu-id="c4a8b-132">En este ejemplo se muestra cómo se puede utilizar el método **Requery** para actualizar una consulta después de cambiar los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset2 
     Dim rstChange As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS ViewCountry Text; " & _ 
     "SELECT FirstName, LastName, Country FROM " & _ 
     "Employees WHERE Country = [ViewCountry] " & _ 
     "ORDER BY LastName") 
     
     qdfTemp.Parameters!ViewCountry = "USA" 
     Debug.Print "Data after initial query, " & _ 
     [ViewCountry] = USA" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Change underlying data. 
     Set rstChange = dbsNorthwind.OpenRecordset("Employees") 
     rstChange.AddNew 
     rstChange!FirstName = "Nina" 
     rstChange!LastName = "Roberts" 
     rstChange!Country = "USA" 
     rstChange.Update 
     
     rstView.Requery 
     Debug.Print "Requery after changing underlying data" 
     Set rstView = qdfTemp.OpenRecordset 
     Do While Not rstView.EOF 
     Debug.Print " " & rstView!FirstName & " " & _ 
     rstView!LastName & ", " & rstView!Country 
     rstView.MoveNext 
     Loop 
     
     ' Restore original data because this is only a 
     ' demonstration. 
     rstChange.Bookmark = rstChange.LastModified 
     rstChange.Delete 
     rstChange.Close 
     
     rstView.Close 
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="c4a8b-133">En este ejemplo se muestra cómo se puede utilizar el método **Requery** para actualizar una consulta después de cambiar los parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="c4a8b-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset2 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfTemp = dbsNorthwind.CreateQueryDef("", _ 
 "PARAMETERS ViewCountry Text; " & _ 
 "SELECT FirstName, LastName, Country FROM " & _ 
 "Employees WHERE Country = [ViewCountry] " & _ 
 "ORDER BY LastName") 
 Set prmCountry = qdfTemp.Parameters!ViewCountry 
 
 qdfTemp.Parameters!ViewCountry = "USA" 
 Debug.Print "Data after initial query, " & _ 
 [ViewCountry] = USA" 
 Set rstView = qdfTemp.OpenRecordset 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 ' Change query parameter. 
 qdfTemp.Parameters!ViewCountry = "UK" 
 ' QueryDef argument must be included so that the 
 ' resulting Recordset reflects the change in the query 
 ' parameter. 
 rstView.Requery qdfTemp 
 Debug.Print "Requery after changing parameter, " & _ 
 "[ViewCountry] = UK" 
 Do While Not rstView.EOF 
 Debug.Print " " & rstView!FirstName & " " & _ 
 rstView!LastName & ", " & rstView!Country 
 rstView.MoveNext 
 Loop 
 
 rstView.Close 
 dbsNorthwind.Close 
 
End Sub 
 
```
