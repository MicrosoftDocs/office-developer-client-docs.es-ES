---
title: Parameter Object (DAO)
TOCTitle: Parameter Object
ms:assetid: 194efd23-6086-13ac-beb9-c2aec101d6fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845640(v=office.15)
ms:contentKeyID: 48543495
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ba1744d1cd740c61c7b80d1a08a73fec317c3a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888569"
---
# <a name="parameter-object-dao"></a><span data-ttu-id="89009-102">Parameter Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="89009-102">Parameter Object (DAO)</span></span>


<span data-ttu-id="89009-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89009-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89009-p101">Un objeto **Parameter** representa un valor suministrado a una consulta. El parámetro está asociado con un objeto **QueryDef** creado a partir de una consulta de parámetros.</span><span class="sxs-lookup"><span data-stu-id="89009-p101">A **Parameter** object represents a value supplied to a query. The parameter is associated with a **QueryDef** object created from a parameter query.</span></span>

## <a name="remarks"></a><span data-ttu-id="89009-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89009-106">Remarks</span></span>

<span data-ttu-id="89009-107">Los objetos **Parameter** permiten cambiar los argumentos de un objeto **QueryDef** ejecutado con frecuencia sin tener que volver a compilar la consulta.</span><span class="sxs-lookup"><span data-stu-id="89009-107">**Parameter** objects allow you to change the arguments in a frequently run **QueryDef** object without having to recompile the query.</span></span>

<span data-ttu-id="89009-p102">Mediante las propiedades de un objeto **Parameter**, puede establecer un parámetro de consulta que se puede cambiar antes de ejecutar la consulta. Se puede:</span><span class="sxs-lookup"><span data-stu-id="89009-p102">Using the properties of a **Parameter** object, you can set a query parameter that can be changed before the query is run. You can:</span></span>

  - <span data-ttu-id="89009-110">Usar la propiedad **Name** para devolver el nombre de un parámetro.</span><span class="sxs-lookup"><span data-stu-id="89009-110">Use the **Name** property to return the name of a parameter.</span></span>

  - <span data-ttu-id="89009-111">Usar la propiedad **Value** para establecer o devolver los valores de parámetros que se utilizarán en la consulta.</span><span class="sxs-lookup"><span data-stu-id="89009-111">Use the **Value** property to set or return the parameter values to be used in the query.</span></span>

  - <span data-ttu-id="89009-112">Usar la propiedad **Type** para devolver el tipo de datos del objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="89009-112">Use the **Type** property to return the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="89009-113">Usar la propiedad **Direction** para establecer o devolver si el parámetro es un parámetro de entrada, un parámetro de salida o ambos.</span><span class="sxs-lookup"><span data-stu-id="89009-113">Use the **Direction** property to set or return whether the parameter is an input parameter, an output parameter, or both.</span></span>

## <a name="example"></a><span data-ttu-id="89009-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="89009-114">Example</span></span>

<span data-ttu-id="89009-p103">En este ejemplo se utilizan objetos **Parameter** y la colección **Parameters** para crear un objeto **QueryDef** temporal y recuperar datos a partir de los cambios efectuados en los **Parameters** del objeto **QueryDef**. Se requiere el procedimiento ParametersChange para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="89009-p103">This example demonstrates **Parameter** objects and the **Parameters** collection by creating a temporary **QueryDef** and retrieving data based on changes made to the **QueryDef** object's **Parameters**. The ParametersChange procedure is required for this procedure to run.</span></span>

```vb
    Sub ParameterX() 
     
     Dim dbsNorthwind As Database 
     Dim qdfReport As QueryDef 
     Dim prmBegin As Parameter 
     Dim prmEnd As Parameter 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create temporary QueryDef object with two 
     ' parameters. 
     Set qdfReport = dbsNorthwind.CreateQueryDef("", _ 
     "PARAMETERS dteBegin DateTime, dteEnd DateTime; " & _ 
     "SELECT EmployeeID, COUNT(OrderID) AS NumOrders " & _ 
     "FROM Orders WHERE ShippedDate BETWEEN " & _ 
     "[dteBegin] AND [dteEnd] GROUP BY EmployeeID " & _ 
     "ORDER BY EmployeeID") 
     Set prmBegin = qdfReport.Parameters!dteBegin 
     Set prmEnd = qdfReport.Parameters!dteEnd 
     
     ' Print report using specified parameter values. 
     ParametersChange qdfReport, prmBegin, #1/1/95#, _ 
     prmEnd, #6/30/95# 
     ParametersChange qdfReport, prmBegin, #7/1/95#, _ 
     prmEnd, #12/31/95# 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub ParametersChange(qdfTemp As QueryDef, _ 
     prmFirst As Parameter, dteFirst As Date, _ 
     prmLast As Parameter, dteLast As Date) 
     ' Report function for ParameterX. 
     
     Dim rstTemp As Recordset 
     Dim fldLoop As Field 
     
     ' Set parameter values and open recordset from 
     ' temporary QueryDef object. 
     prmFirst = dteFirst 
     prmLast = dteLast 
     Set rstTemp = _ 
     qdfTemp.OpenRecordset(dbOpenForwardOnly) 
     Debug.Print "Period " & dteFirst & " to " & dteLast 
     
     ' Enumerate recordset. 
     Do While Not rstTemp.EOF 
     
     ' Enumerate Fields collection of recordset. 
     For Each fldLoop In rstTemp.Fields 
     Debug.Print " - " & fldLoop.Name & " = " & fldLoop; 
     Next fldLoop 
     
     Debug.Print 
     rstTemp.MoveNext 
     Loop 
     
     rstTemp.Close 
     
    End Sub
```
