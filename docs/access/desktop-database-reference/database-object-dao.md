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
# <a name="database-object-dao"></a>Objeto de base de datos (DAO)

**Se aplica a:** Access 2013, Office 2013

Un objeto **Database** representa una base de datos abierta.

## <a name="remarks"></a>Observaciones

El objeto **Database** y sus métodos y propiedades se  usan para manipular una base de datos abierta. En cualquier tipo de base de datos, puede:

  - Usar el método **Execute** para ejecutar una consulta de acciones.

  - Configurar la propiedad **Connect** para establecer una conexión a un origen de datos ODBC.

  - Establecer la propiedad **QueryTimeout** a fin de limitar la duración del tiempo de espera para que se ejecute una consulta en un origen de base de datos ODBC.

  - Usar la propiedad **RecordsAffected** para determinar cuántos registros ha modificado una consulta de acciones.

  - Usar el método **OpenRecordset** para ejecutar una consulta de selección y crear un objeto **Recordset**.

  - Usar la propiedad **Version** para determinar qué versión de un motor de base de datos ha creado la base de datos.

Con la base de datos del motor de base de datos de Microsoft Access, puede usar también otros métodos, propiedades y colecciones para manipular un objeto **Database**, así como crear, modificar u obtener información sobre sus tablas, consultas y relaciones. Por ejemplo, puede:

  - Usar los métodos **CreateTableDef** y **CreateRelation** para crear tablas y relaciones respectivamente.

  - Usar el método **CreateProperty** para definir nuevas propiedades de **Database**.

  - Usar el método **CreateQueryDef** para crear una definición de consulta persistente o temporal.

  - Usar los métodos **MakeReplica**, **Synchronize** y **PopulatePartial** para crear y sincronizar réplicas completas o parciales de la base de datos.

  - Configurar la propiedad **CollatingOrder** para establecer el criterio de ordenación alfabético para los campos basados en caracteres en distintos idiomas.

El método **CreateDatabase** se usa para crear un objeto **Database** persistente que se anexa automáticamente a la colección **Databases** y se guarda, por lo tanto, en el disco.

No necesita especificar el objeto **DBEngine** cuando usa el método **OpenDatabase**.

Al abrir una base de datos con tablas vinculadas, no se establecen automáticamente vínculos con los archivos externos especificados. Debe hacer referencia a los objetos **TableDef** o **Field** de la tabla o abrir un objeto **Recordset**. Si no puede establecer vínculos con estas tablas, se produce un error capturable. Es posible que necesite permisos para tener acceso a la base de datos o que otro usuario tenga la base de datos abierta en modo exclusivo. En estos casos se producen errores capturables.

Cuando se ejecuta un procedimiento que declara un objeto **Database**, los objetos **Database** locales se cierran junto con los objetos **Recordset** abiertos. Se pierden las actualizaciones pendientes y se deshacen las transacciones pendientes, pero no se producen errores capturables. Debe completar explícitamente las transacciones o ediciones pendientes, y cerrar los objetos **Recordset** y **Database** antes de salir de los procedimientos que declaran estas variables de objetos localmente.

Cuando usa uno de los métodos de transacción (**BeginTrans**, **CommitTrans** o **Rollback**) en el objeto **Workspace**, estas transacciones se aplican a todas las bases de datos abiertas en el objeto **Workspace** desde el que se ha abierto el objeto **Database**. Si quiere usar transacciones independientes, primero debe abrir un objeto **Workspace** adicional y, después, abrir otro objeto **Database** en este objeto **Workspace**.


> [!NOTE]
> Puede abrir el mismo origen de datos o base de datos varias veces creando nombres duplicados en la colección **Databases**. Debe asignar objetos **Database** a variables de objeto y hacer referencia a ellas mediante el nombre de variable.



## <a name="example"></a>Ejemplo

En este ejemplo se crea un nuevo objeto **Database** y se abre un objeto **Database** existente en el objeto **Workspace** predeterminado. Después, se enumera la colección **Database** y la colección **Properties** de cada objeto **Database**.

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

En este ejemplo se usa **CreateDatabase** para crear un objeto **Database** nuevo y cifrado.

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
