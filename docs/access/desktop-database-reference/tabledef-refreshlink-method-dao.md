---
title: TableDef.RefreshLink (método) (DAO)
TOCTitle: RefreshLink Method
ms:assetid: 9f0059c6-3b7b-57e3-7527-ef674ad9417d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198349(v=office.15)
ms:contentKeyID: 48546674
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052980
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 8b7fda0c095a04d2a3ab7f295497cff05a620ea6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922541"
---
# <a name="tabledefrefreshlink-method-dao"></a><span data-ttu-id="21a5f-102">TableDef.RefreshLink (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="21a5f-102">TableDef.RefreshLink method (DAO)</span></span>

<span data-ttu-id="21a5f-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21a5f-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="21a5f-104">Actualiza la información de conexión para una tabla vinculada (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="21a5f-104">Updates the connection information for a linked table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="21a5f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21a5f-105">Syntax</span></span>

<span data-ttu-id="21a5f-106">*expresión* . RefreshLink</span><span class="sxs-lookup"><span data-stu-id="21a5f-106">*expression* .RefreshLink</span></span>

<span data-ttu-id="21a5f-107">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="21a5f-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="21a5f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21a5f-108">Remarks</span></span>

<span data-ttu-id="21a5f-p101">Para cambiar la información de conexión para una tabla vinculada, restablezca la propiedad **[Connect](connection-connect-property-dao.md)** del objeto **TableDef** correspondiente y utilice el método **RefreshLink** para actualizar la información. El uso del método **RefreshLink** no cambia las propiedades de la tabla vinculada ni los objetos **[Relation](relation-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="21a5f-p101">To change the connection information for a linked table, reset the **[Connect](connection-connect-property-dao.md)** property of the corresponding **TableDef** object and then use the **RefreshLink** method to update the information. Using **RefreshLink** method doesn't change the linked table's properties and **[Relation](relation-object-dao.md)** objects.</span></span>

<span data-ttu-id="21a5f-111">Para que esta información exista en todas las colecciones asociadas con el objeto **TableDef** que representa la tabla vinculada, debe utilizar el método **[Refresh](tabledefs-refresh-method-dao.md)** en cada colección.</span><span class="sxs-lookup"><span data-stu-id="21a5f-111">For this connection information to exist in all collections associated with the **TableDef** object that represents the linked table, you must use the **[Refresh](tabledefs-refresh-method-dao.md)** method on each collection.</span></span>

## <a name="example"></a><span data-ttu-id="21a5f-112">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="21a5f-112">Example</span></span>

<span data-ttu-id="21a5f-p102">En este ejemplo se utiliza el método **RefreshLink** para actualizar los datos de una tabla vinculada después de cambiar la conexión de un origen de datos a otro. Se requiere el procedimiento RefreshLinkOutput para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="21a5f-p102">This example uses the **RefreshLink** method to refresh the data in a linked table after its connection has been changed from one data source to another. The RefreshLinkOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RefreshLinkX() 
 
 Dim dbsCurrent As Database 
 Dim tdfLinked As TableDef 
 
 ' Open a database to which a linked table can be 
 ' appended. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a linked table that points to a Microsoft 
 ' SQL Server database. 
 Set tdfLinked = _ 
 dbsCurrent.CreateTableDef("AuthorsTable") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 tdfLinked.SourceTableName = "authors" 
 dbsCurrent.TableDefs.Append tdfLinked 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to first source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Change connection information for linked table and 
 ' refresh the connection in order to make the new data 
 ' available. 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 tdfLinked.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=NewPublishers" 
 tdfLinked.RefreshLink 
 
 ' Display contents of linked table. 
 Debug.Print _ 
 "Data from linked table connected to second source:" 
 RefreshLinkOutput dbsCurrent 
 
 ' Delete linked table because this is a demonstration. 
 dbsCurrent.TableDefs.Delete tdfLinked.Name 
 
 dbsCurrent.Close 
 
End Sub 
 
Sub RefreshLinkOutput(dbsTemp As Database) 
 
 Dim rstRemote As Recordset 
 Dim intCount As Integer 
 
 ' Open linked table. 
 Set rstRemote = _ 
 dbsTemp.OpenRecordset("AuthorsTable") 
 
 intCount = 0 
 
 ' Enumerate Recordset object, but stop at 50 records. 
 With rstRemote 
 Do While Not .EOF And intCount < 50 
 Debug.Print , .Fields(0), .Fields(1) 
 intCount = intCount + 1 
 .MoveNext 
 Loop 
 If Not .EOF Then Debug.Print , "[more records]" 
 .Close 
 End With 
 
End Sub 
 
```

