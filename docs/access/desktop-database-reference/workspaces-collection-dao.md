---
title: Colección de áreas de trabajo (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4c615be9e92a936486c15377514c2b695f68bb5b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698417"
---
# <a name="workspaces-collection-dao"></a>Colección de áreas de trabajo (DAO)


**Se aplica a**: Access 2013, Office 2013

Una colección **Workspaces** contiene todos los objetos **Workspace** activos que no están ocultos del objeto **DBEngine**. (Los objetos **Workspace** ocultos no se agregan a la colección y se hace referencia a ellos mediante la variable a la que están asignados.)

## <a name="remarks"></a>Observaciones

Utilice el objeto **Workspace** para administrar la sesión actual o para iniciar una sesión adicional.

Cuando en primer lugar, consulte o usar un objeto **Workspace** , se crea automáticamente el área de trabajo de forma predeterminada, DBEngine.Workspaces(0). Los valores de las propiedades **Name** y **UserName** del área de trabajo predeterminada son "\#área de trabajo predeterminada\#" y "Admin", respectivamente. Si está habilitada la seguridad, el valor de la propiedad **UserName** es el nombre del usuario que ha iniciado sesión.

Puede crear nuevos objetos **Workspace** con el método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)**. Después de crear un nuevo objeto **Workspace**, debe agregarlo a la colección **Workspaces** si necesita hacer referencia a él desde la colección **Workspaces**. Sin embargo, puede utilizar un objeto **Workspace** recién creado sin agregarlo a la colección **Workspaces**.

Para hacer referencia a un objeto **Workspace** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:

**DBEngine**. **Áreas de trabajo** (0)

**DBEngine**. **Áreas de trabajo** ("nombre")

**DBEngine**. **Áreas de trabajo** \! \[nombre\]


> [!NOTE]
> [!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.



## <a name="example"></a>Ejemplo

En este ejemplo, se crea un nuevo objeto Workspace de Microsoft Access y se lo anexa a la colección **Workspaces**. Luego se enumeran las colecciones **Workspaces** y la colección **Properties** del objeto **Workspace**.

```vb 
Sub WorkspaceX() 
 
 Dim wrkNewAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 ' Create a new Microsoft Access workspace. 
 Set wrkNewAcc = CreateWorkspace("NewAccessWorkspace", _ 
 "admin", "", dbUseJet) 
 Workspaces.Append wrkNewAcc 
 
 ' Enumerate the Workspaces collection. 
 For Each wrkLoop In Workspaces 
 With wrkLoop 
 Debug.Print "Properties of " & .Name 
 ' Enumerate the Properties collection of the new 
 ' Workspace object. 
 For Each prpLoop In .Properties 
 On Error Resume Next 
 If prpLoop <> "" Then Debug.Print " " & _ 
 prpLoop.Name & " = " & prpLoop 
 On Error GoTo 0 
 Next prpLoop 
 End With 
 Next wrkLoop 
 
 wrkNewAcc.Close 
End Sub 
```

<br/>

En este ejemplo, se usa el método **CreateWorkspace** para crear un área de trabajo de Microsoft Access. A continuación, se enumeran las propiedades del área de trabajo.

```vb 
Sub CreateWorkspaceX() 
 
 Dim wrkAcc As Workspace 
 Dim wrkLoop As Workspace 
 Dim prpLoop As Property 
 
 
 DefaultType = dbUseJet 
 ' Create an unnamed Workspace object of the type 
 ' specified by the DefaultType property of DBEngine 
 ' (dbUseJet). 
 Set wrkAcc = CreateWorkspace("", "admin", "") 
 
 ' Enumerate Workspaces collection. 
 Debug.Print "Workspace objects in Workspaces collection:" 
 For Each wrkLoop In Workspaces 
 Debug.Print " " & wrkLoop.Name 
 Next wrkLoop 
 
 With wrkAcc 
 ' Enumerate Properties collection of Microsoft Access 
 ' workspace. 
 Debug.Print _ 
 "Properties of unnamed Microsoft Access workspace" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 
 wrkAcc.Close 
 
End Sub 
 
```

