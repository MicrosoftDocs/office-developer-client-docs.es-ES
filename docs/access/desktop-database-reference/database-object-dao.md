---
title: Objeto de base de datos (DAO)
TOCTitle: Database Object
ms:assetid: 6cf2ddf8-3957-a15e-5eeb-85f81c1e415e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195520(v=office.15)
ms:contentKeyID: 48545482
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm0
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c23772c54f2f980b8d10d4afc352687935840752
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294844"
---
# <a name="database-object-dao"></a><span data-ttu-id="3ce3a-102">Objeto de base de datos (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ce3a-102">Database Object (DAO)</span></span>

<span data-ttu-id="3ce3a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ce3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ce3a-104">Un objeto **Database** representa una base de datos abierta.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-104">A **Database** object represents an open database.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ce3a-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ce3a-105">Remarks</span></span>

<span data-ttu-id="3ce3a-p101">El objeto **Database** y sus métodos y propiedades se  usan para manipular una base de datos abierta. En cualquier tipo de base de datos, puede:</span><span class="sxs-lookup"><span data-stu-id="3ce3a-p101">You use the **Database** object and its methods and properties to manipulate an open database. In any type of database, you can:</span></span>

  - <span data-ttu-id="3ce3a-108">Usar el método **Execute** para ejecutar una consulta de acciones.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-108">Use the **Execute** method to run an action query.</span></span>

  - <span data-ttu-id="3ce3a-109">Configurar la propiedad **Connect** para establecer una conexión a un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-109">Set the **Connect** property to establish a connection to an ODBC data source.</span></span>

  - <span data-ttu-id="3ce3a-110">Establecer la propiedad **QueryTimeout** a fin de limitar la duración del tiempo de espera para que se ejecute una consulta en un origen de base de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-110">Set the **QueryTimeout** property to limit the length of time to wait for a query to execute against an ODBC data source.</span></span>

  - <span data-ttu-id="3ce3a-111">Usar la propiedad **RecordsAffected** para determinar cuántos registros ha modificado una consulta de acciones.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-111">Use the **RecordsAffected** property to determine how many records were changed by an action query.</span></span>

  - <span data-ttu-id="3ce3a-112">Usar el método **OpenRecordset** para ejecutar una consulta de selección y crear un objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-112">Use the **OpenRecordset** method to execute a select query and create a **Recordset** object.</span></span>

  - <span data-ttu-id="3ce3a-113">Usar la propiedad **Version** para determinar qué versión de un motor de base de datos ha creado la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-113">Use the **Version** property to determine which version of a database engine created the database.</span></span>

<span data-ttu-id="3ce3a-p102">Con la base de datos del motor de base de datos de Microsoft Access, puede usar también otros métodos, propiedades y colecciones para manipular un objeto **Database**, así como crear, modificar u obtener información sobre sus tablas, consultas y relaciones. Por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="3ce3a-p102">With a Microsoft Access database engine database, you can also use other methods, properties, and collections to manipulate a **Database** object, as well as create, modify, or get information about its tables, queries, and relationships. For example, you can:</span></span>

  - <span data-ttu-id="3ce3a-116">Usar los métodos **CreateTableDef** y **CreateRelation** para crear tablas y relaciones respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-116">Use the **CreateTableDef** and **CreateRelation** methods to create tables and relations, respectively.</span></span>

  - <span data-ttu-id="3ce3a-117">Usar el método **CreateProperty** para definir nuevas propiedades de **Database**.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-117">Use the **CreateProperty** method to define new **Database** properties.</span></span>

  - <span data-ttu-id="3ce3a-118">Usar el método **CreateQueryDef** para crear una definición de consulta persistente o temporal.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-118">Use the **CreateQueryDef** method to create a persistent or temporary query definition.</span></span>

  - <span data-ttu-id="3ce3a-119">Usar los métodos **MakeReplica**, **Synchronize** y **PopulatePartial** para crear y sincronizar réplicas completas o parciales de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-119">Use **MakeReplica**, **Synchronize**, and **PopulatePartial** methods to create and synchronize full or partial replicas of your database.</span></span>

  - <span data-ttu-id="3ce3a-120">Configurar la propiedad **CollatingOrder** para establecer el criterio de ordenación alfabético para los campos basados en caracteres en distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-120">Set the **CollatingOrder** property to establish the alphabetic sorting order for character-based fields in different languages.</span></span>

<span data-ttu-id="3ce3a-121">El método **CreateDatabase** se usa para crear un objeto **Database** persistente que se anexa automáticamente a la colección **Databases** y se guarda, por lo tanto, en el disco.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-121">You use the **CreateDatabase** method to create a persistent **Database** object that is automatically appended to the **Databases** collection, thereby saving it to disk.</span></span>

<span data-ttu-id="3ce3a-122">No necesita especificar el objeto **DBEngine** cuando usa el método **OpenDatabase**.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-122">You don't need to specify the **DBEngine** object when you use the **OpenDatabase** method.</span></span>

<span data-ttu-id="3ce3a-p103">Al abrir una base de datos con tablas vinculadas, no se establecen automáticamente vínculos con los archivos externos especificados. Debe hacer referencia a los objetos **TableDef** o **Field** de la tabla o abrir un objeto **Recordset**. Si no puede establecer vínculos con estas tablas, se produce un error capturable. Es posible que necesite permisos para tener acceso a la base de datos o que otro usuario tenga la base de datos abierta en modo exclusivo. En estos casos se producen errores capturables.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-p103">Opening a database with linked tables doesn't automatically establish links to the specified external files. You must either reference the table's **TableDef** or **Field** objects or open a **Recordset** object. If you can't establish links to these tables, a trappable error occurs. You may also need permission to access the database, or another user might have the database opened exclusively. In these cases, trappable errors occur.</span></span>

<span data-ttu-id="3ce3a-p104">Cuando se ejecuta un procedimiento que declara un objeto **Database**, los objetos **Database** locales se cierran junto con los objetos **Recordset** abiertos. Se pierden las actualizaciones pendientes y se deshacen las transacciones pendientes, pero no se producen errores capturables. Debe completar explícitamente las transacciones o ediciones pendientes, y cerrar los objetos **Recordset** y **Database** antes de salir de los procedimientos que declaran estas variables de objetos localmente.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-p104">When a procedure that declares a **Database** object has executed, local **Database** objects are closed along with any open **Recordset** objects. Any pending updates are lost and any pending transactions are rolled back, but no trappable error occurs. You should explicitly complete any pending transactions or edits and close **Recordset** objects and **Database** objects before exiting procedures that declare these object variables locally.</span></span>

<span data-ttu-id="3ce3a-p105">Cuando usa uno de los métodos de transacción (**BeginTrans**, **CommitTrans** o **Rollback**) en el objeto **Workspace**, estas transacciones se aplican a todas las bases de datos abiertas en el objeto **Workspace** desde el que se ha abierto el objeto **Database**. Si quiere usar transacciones independientes, primero debe abrir un objeto **Workspace** adicional y, después, abrir otro objeto **Database** en este objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-p105">When you use one of the transaction methods (**BeginTrans**, **CommitTrans**, or **Rollback**) on the **Workspace** object, these transactions apply to all databases opened on the **Workspace** from which the **Database** object was opened. If you want to use independent transactions, you must first open an additional **Workspace** object, and then open another **Database** object in that **Workspace** object.</span></span>


> [!NOTE]
> <span data-ttu-id="3ce3a-p106">Puede abrir el mismo origen de datos o base de datos varias veces creando nombres duplicados en la colección **Databases**. Debe asignar objetos **Database** a variables de objeto y hacer referencia a ellas mediante el nombre de variable.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-p106">You can open the same data source or database more than once, creating duplicate names in the **Databases** collection. You should assign **Database** objects to object variables and refer to them by variable name.</span></span>



## <a name="example"></a><span data-ttu-id="3ce3a-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ce3a-135">Example</span></span>

<span data-ttu-id="3ce3a-p107">En este ejemplo se crea un nuevo objeto **Database** y se abre un objeto **Database** existente en el objeto **Workspace** predeterminado. Después, se enumera la colección **Database** y la colección **Properties** de cada objeto **Database**.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-p107">This example creates a new **Database** object and opens an existing **Database** object in the default **Workspace** object. Then it enumerates the **Database** collection and the **Properties** collection of each **Database** object.</span></span>

```vb 
Sub DatabaseObjectX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim dbsNew As Database 
 Dim dbsLoop As Database 
 Dim prpLoop As Property 
 
 Set wrkAcc = CreateWorkspace("AccessWorkspace", "admin", _ 
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

<span data-ttu-id="3ce3a-138">En este ejemplo se usa **CreateDatabase** para crear un objeto **Database** nuevo y cifrado.</span><span class="sxs-lookup"><span data-stu-id="3ce3a-138">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

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
