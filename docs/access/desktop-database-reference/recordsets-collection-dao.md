---
title: Colección Recordsets (DAO)
TOCTitle: Recordsets Collection
ms:assetid: 246d9a78-4ce8-6393-982b-77ac00cd85bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191819(v=office.15)
ms:contentKeyID: 48543756
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b935e05264497c7ad09ada4a8c50c775845857b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309313"
---
# <a name="recordsets-collection-dao"></a><span data-ttu-id="cb603-102">Colección Recordsets (DAO)</span><span class="sxs-lookup"><span data-stu-id="cb603-102">Recordsets collection (DAO)</span></span>

<span data-ttu-id="cb603-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb603-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb603-104">Una colección **Recordsets** contiene todos los objetos **Recordset** abiertos en un objeto **Connection** o **Database**.</span><span class="sxs-lookup"><span data-stu-id="cb603-104">A **Recordsets** collection contains all open **Recordset** objects in a **Connection** or **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb603-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cb603-105">Remarks</span></span>

<span data-ttu-id="cb603-106">Cuando se utilizan objetos de DAO, los datos se tratan casi siempre mediante objetos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cb603-106">When you use DAO objects, you manipulate data almost entirely using **Recordset** objects.</span></span>

<span data-ttu-id="cb603-107">Un objeto **Recordset** nuevo se agrega automáticamente a la colección **Recordsets** cuando se abre el objeto **Recordset** y se quita automáticamente cuando se cierra.</span><span class="sxs-lookup"><span data-stu-id="cb603-107">A new **Recordset** object is automatically added to the **Recordsets** collection when you open the **Recordset** object, and is automatically removed when you close it.</span></span>

<span data-ttu-id="cb603-p101">Se pueden crear tantas variables del objeto **Recordset** como sean necesarias. Diferentes objetos **Recordset** pueden tener acceso a las mismas tablas, consultas y campos sin entrar en conflicto.</span><span class="sxs-lookup"><span data-stu-id="cb603-p101">You can create as many **Recordset** object variables as needed. Different **Recordset** objects can access the same tables, queries, and fields without conflicting.</span></span>

<span data-ttu-id="cb603-110">Para hacer referencia a un objeto **Recordset** de una colección por su número ordinal o el valor de su propiedad **Name**, utilice cualquiera de las siguientes formas de sintaxis:</span><span class="sxs-lookup"><span data-stu-id="cb603-110">To refer to a **Recordset** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="cb603-111">**Recordsets**(0)</span><span class="sxs-lookup"><span data-stu-id="cb603-111">**Recordsets**(0)</span></span>

- <span data-ttu-id="cb603-112">**Recordsets**("nombre")</span><span class="sxs-lookup"><span data-stu-id="cb603-112">**Recordsets**("name")</span></span>

- <span data-ttu-id="cb603-113">**Recordsets**\!\[nombre\]</span><span class="sxs-lookup"><span data-stu-id="cb603-113">**Recordsets**\!\[name\]</span></span>

> [!NOTE]
> <span data-ttu-id="cb603-p102">Puede abrir un objeto **Recordset** desde la misma base de datos o el mismo origen de datos varias veces, creando nombres duplicados en la colección **Recordsets**. Debe asignar objetos **Recordset** a variables de objeto y hacer referencia a ellos por el nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="cb603-p102">You can open a **Recordset** object from the same data source or database more than once, creating duplicate names in the **Recordsets** collection. You should assign **Recordset** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="cb603-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb603-116">Example</span></span>

<span data-ttu-id="cb603-117">A continuación se ofrece una demostración de objetos **Recordset** y la colección **Recordsets**. En este ejemplo, se abren cuatro tipos diferentes de objetos **Recordsets**, se enumera la colección Recordsets del objeto **Database** actual y se enumera la colección **Properties** de cada objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="cb603-117">This example demonstrates **Recordset** objects and the **Recordsets** collection by opening four different types of **Recordsets**, enumerating the Recordsets collection of the current **Database**, and enumerating the **Properties** collection of each **Recordset**.</span></span>

```vb
    Sub RecordsetX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTable As Recordset 
     Dim rstDynaset As Recordset 
     Dim rstSnapshot As Recordset 
     Dim rstForwardOnly As Recordset 
     Dim rstLoop As Recordset 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Open one of each type of Recordset object. 
     Set rstTable = .OpenRecordset("Categories", _ 
     dbOpenTable) 
     Set rstDynaset = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstSnapshot = .OpenRecordset("Shippers", _ 
     dbOpenSnapshot) 
     Set rstForwardOnly = .OpenRecordset _ 
     ("Employees", dbOpenForwardOnly) 
     
     Debug.Print "Recordsets in Recordsets " & _ 
     "collection of dbsNorthwind" 
     
     ' Enumerate Recordsets collection. 
     For Each rstLoop In .Recordsets 
     
     With rstLoop 
     Debug.Print " " & .Name 
     
     ' Enumerate Properties collection of each 
     ' Recordset object. Trap for any 
     ' properties whose values are invalid in 
     ' this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     If prpLoop <> "" Then Debug.Print _ 
     " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     End With 
     
     Next rstLoop 
     
     rstTable.Close 
     rstDynaset.Close 
     rstSnapshot.Close 
     rstForwardOnly.Close 
     
     .Close 
     End With 
     
    End Sub
```
