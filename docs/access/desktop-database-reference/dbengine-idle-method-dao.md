---
title: DBEngine.Idle (método) (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 68c0e6d246370f9c4f0c241195fb19c241ca49e5
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949722"
---
# <a name="dbengineidle-method-dao"></a><span data-ttu-id="806a5-102">DBEngine.Idle (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="806a5-102">DBEngine.Idle method (DAO)</span></span>

<span data-ttu-id="806a5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="806a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="806a5-104">Suspende el procesamiento de datos y habilita el motor de base de datos de Microsoft Access para que realice las tareas pendientes, como la optimización de memoria o los tiempos de espera de paginación (sólo en áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="806a5-104">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="806a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="806a5-105">Syntax</span></span>

<span data-ttu-id="806a5-106">*expresión* . Inactivo (***acción***)</span><span class="sxs-lookup"><span data-stu-id="806a5-106">*expression* .Idle(***Action***)</span></span>

<span data-ttu-id="806a5-107">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="806a5-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="806a5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="806a5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="806a5-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="806a5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="806a5-110">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="806a5-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="806a5-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="806a5-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="806a5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="806a5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="806a5-113"><em>Acción</em></span><span class="sxs-lookup"><span data-stu-id="806a5-113"><em>Action</em></span></span></p></td>
<td><p><span data-ttu-id="806a5-114">Opcional</span><span class="sxs-lookup"><span data-stu-id="806a5-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="806a5-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="806a5-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="806a5-p101">Especifica la acción que se va a realizar. Puede ser una de las constantes <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="806a5-p101">Specifies the action to take. Can be one of the <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="806a5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="806a5-118">Remarks</span></span>

<span data-ttu-id="806a5-p102">El método **Idle** permite que el motor de base de datos de Microsoft Access realice tareas en segundo plano que pueden no estar actualizadas debido al procesamiento de una gran cantidad de datos. Esto suele ocurrir en los entornos multitarea y multiusuario que no disponen de tiempo de procesamiento en segundo plano suficiente para mantener todos los registros en un objeto **[Recordset](recordset-object-dao.md)** actual.</span><span class="sxs-lookup"><span data-stu-id="806a5-p102">The **Idle** method allows the Microsoft Access database engine to perform background tasks that may not be up-to-date because of intense data processing. This is often true in multiuser, multitasking environments that don't have enough background processing time to keep all records in a **[Recordset](recordset-object-dao.md)** current.</span></span>

<span data-ttu-id="806a5-p103">Normalmente, se quitan los bloqueos de lectura y los datos de los objetos **Recordset** locales de tipo dynaset solo se actualizan cuando no se produce ninguna otra acción (ni siquiera movimientos del mouse). Si usa con frecuencia el método **Idle**, el motor de base de datos de Microsoft Access puede ocuparse de las tareas de procesamiento en segundo plano liberando bloqueos de lectura innecesarios.</span><span class="sxs-lookup"><span data-stu-id="806a5-p103">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur. If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span></span>

<span data-ttu-id="806a5-123">Al especificar el argumento **dbRefreshCache** opcional, la memoria se actualiza solamente con los datos más actuales de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="806a5-123">Specifying the optional **dbRefreshCache** argument refreshes memory with only the most current data from the database.</span></span>

<span data-ttu-id="806a5-p104">No es necesario utilizar este método en entornos de un solo usuario a no ser que se ejecuten varias instancias de una aplicación. El método puede **Idle** mejorar el rendimiento en un entorno multiusuario, ya que fuerza al motor de base de datos a escribir datos en disco liberando bloqueos de la memoria.</span><span class="sxs-lookup"><span data-stu-id="806a5-p104">You don't need to use this method in single-user environments unless multiple instances of an application are running. The **Idle** method may increase performance in a multiuser environment because it forces the database engine to write data to disk, releasing locks on memory.</span></span>


> [!NOTE]
> <span data-ttu-id="806a5-126">[!NOTA] Puede liberar también bloqueos de lectura convirtiendo las operaciones en parte de una transacción.</span><span class="sxs-lookup"><span data-stu-id="806a5-126">You can also release read locks by making operations part of a transaction.</span></span>

## <a name="example"></a><span data-ttu-id="806a5-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="806a5-127">Example</span></span>

<span data-ttu-id="806a5-p105">En este ejemplo se utiliza el método **Idle** para garantizar que un procedimiento de salida tiene acceso a los datos más actuales disponibles de la base de datos. Se requiere el procedimiento IdleOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="806a5-p105">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database. The IdleOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

