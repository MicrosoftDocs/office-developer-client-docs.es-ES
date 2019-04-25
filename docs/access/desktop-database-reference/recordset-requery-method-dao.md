---
title: Método Recordset.Requery (DAO)
TOCTitle: Requery Method
ms:assetid: a5d66eb5-499c-4133-f6c3-c7a1619a8a11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821155(v=office.15)
ms:contentKeyID: 48546840
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: bd6f2fdf7d1f8ba9fc47c6223a8f872a655a1e3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307626"
---
# <a name="recordsetrequery-method-dao"></a><span data-ttu-id="eab97-102">Método Recordset.Requery (DAO)</span><span class="sxs-lookup"><span data-stu-id="eab97-102">Recordset.Requery method (DAO)</span></span>

<span data-ttu-id="eab97-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eab97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eab97-104">Actualiza los datos en un objeto **[Recordset](recordset-object-dao.md)** al volver a ejecutar la consulta en la que se basa el objeto.</span><span class="sxs-lookup"><span data-stu-id="eab97-104">Updates the data in a **[Recordset](recordset-object-dao.md)** object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eab97-105">Syntax</span></span>

<span data-ttu-id="eab97-106">*expression* .Requery(***NewQueryDef***)</span><span class="sxs-lookup"><span data-stu-id="eab97-106">*expression* .Requery(***NewQueryDef***)</span></span>

<span data-ttu-id="eab97-107">*expression* Variable que representa un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="eab97-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="eab97-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="eab97-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eab97-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="eab97-109">Name</span></span></p></th>
<th><p><span data-ttu-id="eab97-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="eab97-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="eab97-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="eab97-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="eab97-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="eab97-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eab97-113"><em>NewQueryDef</em></span><span class="sxs-lookup"><span data-stu-id="eab97-113"><em>NewQueryDef</em></span></span></p></td>
<td><p><span data-ttu-id="eab97-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="eab97-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="eab97-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="eab97-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="eab97-116">Representa el valor de la propiedad <strong>Name</strong> de un objeto <strong><a href="querydef-object-dao.md">QueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="eab97-116">Represents the <strong>Name</strong> property value of a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="eab97-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eab97-117">Remarks</span></span>

<span data-ttu-id="eab97-118">Use este método para asegurarse de que un **Recordset** contiene los datos más recientes.</span><span class="sxs-lookup"><span data-stu-id="eab97-118">Use this method to make sure that a **Recordset** contains the most recent data.</span></span> <span data-ttu-id="eab97-119">Este método rellena el objeto **Recordset** usando los parámetros de consulta actuales o (en un área de trabajo de Microsoft Access) los nuevos parámetros proporcionados por el argumento newquerydef.</span><span class="sxs-lookup"><span data-stu-id="eab97-119">This method re-populates the current **Recordset** by using either the current query parameters or (in a Microsoft Access workspace) the new ones supplied by the  newquerydef argument.</span></span>

<span data-ttu-id="eab97-120">Si no especifica un argumento newquerydef, **Recordset** se rellena basándose en la misma definición de consulta y parámetros que se usaron originalmente para llenar **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="eab97-120">If you don't specify a  newquerydef argument, the **Recordset** is re-populated based on the same query definition and parameters used to originally populate the **Recordset**.</span></span> <span data-ttu-id="eab97-121">Cualquier cambio en los datos subyacentes se reflejará durante este nuevo relleno.</span><span class="sxs-lookup"><span data-stu-id="eab97-121">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="eab97-122">Si no usó **QueryDef** para crear **Recordset**, **Recordset** se vuelve a crear desde cero.</span><span class="sxs-lookup"><span data-stu-id="eab97-122">If you didn't use a **QueryDef** to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="eab97-123">Si especifica el objeto **QueryDef** original en el argumento newquerydef, se vuelve a consultar **Recordset** mediante los parámetros especificados por **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="eab97-123">If you specify the original **QueryDef** in the  newquerydef argument, then the **Recordset** is requeried using the parameters specified by the **QueryDef**.</span></span> <span data-ttu-id="eab97-124">Los cambios realizados en los datos subyacentes se reflejarán durante este nuevo relleno.</span><span class="sxs-lookup"><span data-stu-id="eab97-124">Any changes to the underlying data will be reflected during this re-population.</span></span> <span data-ttu-id="eab97-125">Para reflejar cualquier cambio en los valores de los parámetros de consulta en **Recordset**, debe proporcionar el argumento newquerydef.</span><span class="sxs-lookup"><span data-stu-id="eab97-125">To reflect any changes to the query parameter values in the **Recordset**, you must supply the  newquerydef argument.</span></span>

<span data-ttu-id="eab97-126">Si especifica un objeto **QueryDef** diferente al que se usó originalmente para crear **Recordset**, **Recordset** se vuelve a crear desde cero.</span><span class="sxs-lookup"><span data-stu-id="eab97-126">If you specify a different **QueryDef** than what was originally used to create the **Recordset**, the **Recordset** is re-created from scratch.</span></span>

<span data-ttu-id="eab97-127">Cuando usa **Requery**, el primer registro de **Recordset** se convierte en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="eab97-127">When you use **Requery**, the first record in the **Recordset** becomes the current record.</span></span>

<span data-ttu-id="eab97-128">No puede usar el método **Requery** en objetos **Recordset** de tipo dynaset o snapshot cuya propiedad **[Restartable](recordset-restartable-property-dao.md)** está establecida en **False**.</span><span class="sxs-lookup"><span data-stu-id="eab97-128">You can't use the **Requery** method on dynaset- or snapshot-type **Recordset** objects whose **[Restartable](recordset-restartable-property-dao.md)** property is set to **False**.</span></span> <span data-ttu-id="eab97-129">No obstante, si proporciona el argumento opcional newquerydef, se omite la propiedad **Restartable**.</span><span class="sxs-lookup"><span data-stu-id="eab97-129">However, if you supply the optional  newquerydef argument, the **Restartable** property is ignored.</span></span>

<span data-ttu-id="eab97-130">Si los dos valores de las propiedades **[BOF](recordset-bof-property-dao.md)** y **[EOF](recordset-eof-property-dao.md)** del objeto **Recordset** son **True** después de usar el método **Requery**, la consulta no devuelve ningún registro y **Recordset** no contiene datos.</span><span class="sxs-lookup"><span data-stu-id="eab97-130">If both the **[BOF](recordset-bof-property-dao.md)** and **[EOF](recordset-eof-property-dao.md)** property settings of the **Recordset** object are **True** after you use the **Requery** method, the query didn't return any records and the **Recordset** contains no data.</span></span>

## <a name="example"></a><span data-ttu-id="eab97-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eab97-131">Example</span></span>

<span data-ttu-id="eab97-132">Este ejemplo muestra cómo el método **Requery** puede usarse para actualizar una consulta después de cambiar los datos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="eab97-132">This example shows how the **Requery** method can be used to refresh a query after underlying data has been changed.</span></span>

```vb
    Sub RequeryX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfTemp As QueryDef 
     Dim rstView As Recordset 
     Dim rstChange As Recordset 
     
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

<span data-ttu-id="eab97-133">En este ejemplo se muestra cómo se puede utilizar el método **Requery** para actualizar una consulta después de cambiar los parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="eab97-133">This example shows how the **Requery** method can be used to refresh a query after the query parameters have been changed.</span></span>

```vb 
Sub RequeryX2() 
 
 Dim dbsNorthwind As Database 
 Dim qdfTemp As QueryDef 
 Dim prmCountry As Parameter 
 Dim rstView As Recordset 
 
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

