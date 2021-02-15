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
# <a name="databases-collection-dao"></a>Colección Databases (DAO)

**Se aplica a:** Access 2013, Office 2013

Una colección **Databases** contiene todos los objetos **Database** abiertos o creados en un objeto **Workspace**.

## <a name="remarks"></a>Comentarios

Al abrir un objeto **Database** existente o crear uno nuevo desde un objeto **Workspace**, éste se agrega automáticamente a la colección **Databases**. Al cerrar un objeto **Database** con el método **[Close](connection-close-method-dao.md)**, éste se quita de la colección **Databases** pero no se elimina del disco. Debe cerrar todos los objetos **Recordset** abiertos antes de cerrar un objeto **Database**.

En un área de trabajo de Microsoft Access, el valor de la propiedad **Name** de una base de datos es una cadena que especifica la ruta del archivo de base de datos.

Para hacer referencia a un objeto **Database** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

- **Bases de** datos (0)

- **Bases de** datos ("*nombre*")

- **Bases de datos** \! \[ *name*\]

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
