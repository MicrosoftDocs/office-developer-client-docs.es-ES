---
title: Propiedad Parameter.Direction (DAO)
TOCTitle: Direction Property
ms:assetid: b78c87ff-1181-21ef-7126-92d309751005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822422(v=office.15)
ms:contentKeyID: 48547300
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053586
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3260fd3f01e8ca22d5be4f8d14f6376c31e2735a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288094"
---
# <a name="parameterdirection-property-dao"></a><span data-ttu-id="c87c1-102">Propiedad Parameter.Direction (DAO)</span><span class="sxs-lookup"><span data-stu-id="c87c1-102">Parameter.Direction property (DAO)</span></span>


<span data-ttu-id="c87c1-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c87c1-103">**Applies to**: Access 2013, Office 2013</span></span>


## <a name="syntax"></a><span data-ttu-id="c87c1-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c87c1-104">Syntax</span></span>

<span data-ttu-id="c87c1-105">*expresión* . Dirección</span><span class="sxs-lookup"><span data-stu-id="c87c1-105">*expression* .Direction</span></span>

<span data-ttu-id="c87c1-106">*expresión* Variable que representa un **objeto Parameter.**</span><span class="sxs-lookup"><span data-stu-id="c87c1-106">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c87c1-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c87c1-107">Remarks</span></span>

<span data-ttu-id="c87c1-108">La configuración o el valor devuelto es un tipo de datos Long que se puede establecer en una de las constantes **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c87c1-108">The setting or return value is a Long that can be set to one of the **[ParameterDirectionEnum](parameterdirectionenum-enumeration-dao.md)** constants.</span></span>

<span data-ttu-id="c87c1-p101">Use la propiedad **Direction** para determinar si el parámetro es un parámetro de entrada, un parámetro de salida, ambos o el valor devuelto del procedimiento. Algunos controladores ODBC no proporcionan información sobre la dirección de los parámetros a una instrucción SELECT o llamada a procedimiento. En estos casos, es necesario establecer la dirección antes de ejecutar la consulta.</span><span class="sxs-lookup"><span data-stu-id="c87c1-p101">Use the **Direction** property to determine whether the parameter is an input parameter, output parameter, both, or the return value from the procedure. Some ODBC drivers do not provide information on the direction of parameters to a SELECT statement or procedure call. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

<span data-ttu-id="c87c1-112">Por ejemplo, el siguiente procedimiento devuelve un valor de un procedimiento almacenado denominado "obtener \_ empleados":</span><span class="sxs-lookup"><span data-stu-id="c87c1-112">For example, the following procedure returns a value from a stored procedure named "get\_employees":</span></span>

<span data-ttu-id="c87c1-113">{?</span><span class="sxs-lookup"><span data-stu-id="c87c1-113">{?</span></span> <span data-ttu-id="c87c1-114">= llamar a obtener \_ empleados}</span><span class="sxs-lookup"><span data-stu-id="c87c1-114">= call get\_employees}</span></span>

<span data-ttu-id="c87c1-p103">Esta llamada produce un parámetro: el valor devuelto. Debe establecer la dirección de este parámetro en **dbParamOutput** o **dbParamReturnValue** antes de ejecutar **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c87c1-p103">This call produces one parameter — the return value. You need to set the direction of this parameter to **dbParamOutput** or **dbParamReturnValue** before executing the **[QueryDef](querydef-object-dao.md)**.</span></span>

<span data-ttu-id="c87c1-117">Debe establecer todas las direcciones de parámetros excepto **dbParamInput** antes de establecer o tener acceso a los valores de los parámetros y antes de ejecutar **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="c87c1-117">You need to set all parameter directions except **dbParamInput** before accessing or setting the values of the parameters and before executing the **QueryDef**.</span></span>

<span data-ttu-id="c87c1-118">Debe usar **dbParamReturnValue** para los valores devueltos, pero en los casos en que el controlador o el servidor no admitan dicha opción, puede usar **dbParamOutput** en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c87c1-118">You should use **dbParamReturnValue** for return values, but in cases where that option is not supported by the driver or the server, you can use **dbParamOutput** instead.</span></span>

<span data-ttu-id="c87c1-p104">El controlador de Microsoft SQL Server establece automáticamente la propiedad **Direction** para todos los parámetros de procedimientos. No todos los controladores ODBC pueden determinar la dirección de un parámetro de consulta. En estos casos, es necesario establecer la dirección antes de ejecutar la consulta.</span><span class="sxs-lookup"><span data-stu-id="c87c1-p104">The Microsoft SQL Server driver automatically sets the **Direction** property for all procedure parameters. Not all ODBC drivers can determine the direction of a query parameter. In these cases, it is necessary to set the direction prior to executing the query.</span></span>

## <a name="example"></a><span data-ttu-id="c87c1-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c87c1-122">Example</span></span>

<span data-ttu-id="c87c1-123">En este ejemplo, se usa la propiedad **Direction** para configurar los parámetros de una consulta en un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="c87c1-123">This example uses the **Direction** property to configure the parameters of a query to an ODBC data source.</span></span>

```vb 
Sub DirectionX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim qdfTemp As QueryDef 
 Dim rstTemp As Recordset 
 Dim strSQL As String 
 Dim intLoop As Integer 
 
 ' Create ODBC workspace and open a connection to a 
 ' Microsoft SQL Server database. 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' Set SQL string to call the stored procedure 
 ' getempsperjob. 
 strSQL = "{ call getempsperjob (?, ?) }" 
 
 Set qdfTemp = conMain.CreateQueryDef("", strSQL) 
 
 With qdfTemp 
 ' Indicate that the two query parameters will only 
 ' pass information to the stored procedure. 
 .Parameters(0).Direction = dbParamInput 
 .Parameters(1).Direction = dbParamInput 
 
 ' Assign initial parameter values. 
 .Parameters(0) = "0877" 
 .Parameters(1) = 0 
 
 Set rstTemp = .OpenRecordset() 
 
 With rstTemp 
 ' Loop through all valid values for the second 
 ' parameter. For each value, requery the recordset 
 ' to obtain the correct results and then print out 
 ' the contents of the recordset. 
 For intLoop = 1 To 14 
 qdfTemp.Parameters(1) = intLoop 
 .Requery 
 Debug.Print "Publisher = " & _ 
 qdfTemp.Parameters(0) & _ 
 ", job = " & intLoop 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 Next intLoop 
 .Close 
 End With 
 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

