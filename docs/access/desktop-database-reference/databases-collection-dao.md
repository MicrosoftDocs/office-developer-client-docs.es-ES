---
title: Colección Databases (DAO)
TOCTitle: Databases Collection
ms:assetid: 988ae6f5-ec15-cd1c-191d-f295624425f4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197944(v=office.15)
ms:contentKeyID: 48546493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbaa0fe7aaa50c8aec582e2f03cd2849268816b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294648"
---
# <a name="databases-collection-dao"></a><span data-ttu-id="1e8e2-102">Colección Databases (DAO)</span><span class="sxs-lookup"><span data-stu-id="1e8e2-102">Databases collection (DAO)</span></span>

<span data-ttu-id="1e8e2-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e8e2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e8e2-104">Una colección **Databases** contiene todos los objetos **Database** abiertos o creados en un objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="1e8e2-104">A **Databases** collection contains all open **Database** objects opened or created in a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e8e2-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e8e2-105">Remarks</span></span>

<span data-ttu-id="1e8e2-p101">Al abrir un objeto **Database** existente o crear uno nuevo desde un objeto **Workspace**, éste se agrega automáticamente a la colección **Databases**. Al cerrar un objeto **Database** con el método **[Close](connection-close-method-dao.md)**, éste se quita de la colección **Databases** pero no se elimina del disco. Debe cerrar todos los objetos **Recordset** abiertos antes de cerrar un objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="1e8e2-p101">When you open an existing **Database** object or create a new one from a **Workspace**, it is automatically appended to the **Databases** collection. When you close a **Database** object with the **[Close](connection-close-method-dao.md)** method, it is removed from the **Databases** collection but not deleted from disk. You should close all open **Recordset** objects before closing a **Database** object.</span></span>

<span data-ttu-id="1e8e2-109">En un área de trabajo de Microsoft Access, el valor de la propiedad **Name** de una base de datos es una cadena que especifica la ruta del archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1e8e2-109">In a Microsoft Access workspace, the **Name** property setting of a database is a string that specifies the path of the database file.</span></span>

<span data-ttu-id="1e8e2-110">Para hacer referencia a un objeto **Database** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="1e8e2-110">To refer to a **Database** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="1e8e2-111">**Bases** de datos (0)</span><span class="sxs-lookup"><span data-stu-id="1e8e2-111">**Databases**(0)</span></span>

- <span data-ttu-id="1e8e2-112">**Bases de datos**("*nombre*")</span><span class="sxs-lookup"><span data-stu-id="1e8e2-112">**Databases**("*name*")</span></span>

- <span data-ttu-id="1e8e2-113">**Bases de datos** \! \[ *nombre*\]</span><span class="sxs-lookup"><span data-stu-id="1e8e2-113">**Databases**\!\[*name*\]</span></span>

> [!NOTE]
> <span data-ttu-id="1e8e2-p102">Puede abrir el mismo origen de datos o base de datos varias veces creando nombres duplicados en la colección **Databases**. Debe asignar objetos **Database** a variables de objeto y hacer referencia a ellas mediante el nombre de variable.</span><span class="sxs-lookup"><span data-stu-id="1e8e2-p102">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>

## <a name="example"></a><span data-ttu-id="1e8e2-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1e8e2-116">Example</span></span>

<span data-ttu-id="1e8e2-p103">En este ejemplo se crea un nuevo objeto **Database** y se abre un objeto **Database** existente en el objeto **Workspace** predeterminado. Después, se enumera la colección **Database** y la colección **Properties** de cada objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="1e8e2-p103">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccWorkspace", "admin", _ 
 "", dbUseJet) 
 
 ' Make sure there isn't already a file with the name of 
 ' the new database. 
 If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
 
 ' Create a new database with the specified 
 ' collating order. 
 Set dbsNew = wrkAcc.CreateDatabase("NewDB.mdb", _ 
 dbLangGeneral) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Enumerate the Databases collection. 
 For Each dbsLoop In wrkAcc.Databases 
 With dbsLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of each 
 ' Database object. 
 For Each prpLoop In .Properties 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 End With 
 Next dbsLoop 
 
 dbsNew.Close 
 dbsNorthwind.Close 
 wrkAcc.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="1e8e2-119">En este ejemplo se usa **CreateDatabase** para crear un objeto **Database** nuevo y cifrado.</span><span class="sxs-lookup"><span data-stu-id="1e8e2-119">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
     Dim wrkDefault As Workspace 
     Dim dbsNew As DATABASE 
     Dim prpLoop As Property 
     
     ' Get default Workspace. 
     Set wrkDefault = DBEngine.Workspaces(0) 
     
     ' Make sure there isn't already a file with the name of 
     ' the new database. 
     If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
     ' Create a new encrypted database with the specified 
     ' collating order. 
     Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
     dbLangGeneral, dbEncrypt) 
     
     With dbsNew 
     Debug.Print "Properties of " & .Name 
     ' Enumerate the Properties collection of the new 
     ' Database object. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     End With 
     
     dbsNew.Close 
     
    End Sub
```
