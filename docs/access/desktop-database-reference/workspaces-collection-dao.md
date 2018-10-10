---
title: Workspaces Collection (DAO)
TOCTitle: Workspaces Collection
ms:assetid: 88b851ce-4180-964f-582e-bc9571bf554c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197057(v=office.15)
ms:contentKeyID: 48546142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37fd4ce04dbd35fccb2356b8088450d07af203d4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484541"
---
# <a name="workspaces-collection-dao"></a><span data-ttu-id="a775f-102">Workspaces Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="a775f-102">Workspaces Collection (DAO)</span></span>


<span data-ttu-id="a775f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a775f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a775f-p101">Una colección **Workspaces** contiene todos los objetos **Workspace** activos que no están ocultos del objeto **DBEngine**. (Los objetos **Workspace** ocultos no se agregan a la colección y se hace referencia a ellos mediante la variable a la que están asignados.)</span><span class="sxs-lookup"><span data-stu-id="a775f-p101">A **Workspaces** collection contains all active, unhidden **Workspace** objects of the **DBEngine** object. (Hidden **Workspace** objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="remarks"></a><span data-ttu-id="a775f-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a775f-106">Remarks</span></span>

<span data-ttu-id="a775f-107">Utilice el objeto **Workspace** para administrar la sesión actual o para iniciar una sesión adicional.</span><span class="sxs-lookup"><span data-stu-id="a775f-107">Use the **Workspace** object to manage the current session or to start an additional session.</span></span>

<span data-ttu-id="a775f-108">Cuando en primer lugar, consulte o usar un objeto **Workspace** , se crea automáticamente el área de trabajo de forma predeterminada, DBEngine.Workspaces(0).</span><span class="sxs-lookup"><span data-stu-id="a775f-108">When you first refer to or use a **Workspace** object, you automatically create the default workspace, DBEngine.Workspaces(0).</span></span> <span data-ttu-id="a775f-109">Los valores de las propiedades **Name** y **UserName** del área de trabajo predeterminada son "\#área de trabajo predeterminada\#" y "Admin", respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a775f-109">The settings of the **Name** and **UserName** properties of the default workspace are "\#Default Workspace\#" and "Admin," respectively.</span></span> <span data-ttu-id="a775f-110">Si está habilitada la seguridad, el valor de la propiedad **UserName** es el nombre del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="a775f-110">If security is enabled, the **UserName** property setting is the name of the user who logged on.</span></span>

<span data-ttu-id="a775f-p103">Puede crear nuevos objetos **Workspace** con el método **[CreateWorkspace](dbengine-createworkspace-method-dao.md)**. Después de crear un nuevo objeto **Workspace**, debe agregarlo a la colección **Workspaces** si necesita hacer referencia a él desde la colección **Workspaces**. Sin embargo, puede utilizar un objeto **Workspace** recién creado sin agregarlo a la colección **Workspaces**.</span><span class="sxs-lookup"><span data-stu-id="a775f-p103">You can create new **Workspace** objects with the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method. After you create a new **Workspace** object, you must append it to the **Workspaces** collection if you need to refer to it from the **Workspaces** collection. You can, however, use a newly created **Workspace** object without appending it to the **Workspaces** collection.</span></span>

<span data-ttu-id="a775f-114">Para hacer referencia a un objeto **Workspace** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a775f-114">To refer to a **Workspace** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="a775f-115">**DBEngine**. **Áreas de trabajo** (0)</span><span class="sxs-lookup"><span data-stu-id="a775f-115">**DBEngine**.**Workspaces**(0)</span></span>

<span data-ttu-id="a775f-116">**DBEngine**. **Áreas de trabajo** ("nombre")</span><span class="sxs-lookup"><span data-stu-id="a775f-116">**DBEngine**.**Workspaces**("name")</span></span>

<span data-ttu-id="a775f-117">**DBEngine**. **Áreas de trabajo** \! \[nombre\]</span><span class="sxs-lookup"><span data-stu-id="a775f-117">**DBEngine**.**Workspaces**\!\[name\]</span></span>


> [!NOTE]
> <span data-ttu-id="a775f-p104">[!NOTA] No se admiten áreas de trabajo de ODBCDirect en Microsoft Access 2013. Use ADO si quiere acceder a orígenes de datos externos sin usar el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a775f-p104">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>



## <a name="example"></a><span data-ttu-id="a775f-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a775f-120">Example</span></span>

<span data-ttu-id="a775f-p105">En este ejemplo, se crea un nuevo objeto Workspace de Microsoft Access y se lo anexa a la colección **Workspaces**. Luego se enumeran las colecciones **Workspaces** y la colección **Properties** del objeto **Workspace**.</span><span class="sxs-lookup"><span data-stu-id="a775f-p105">This example creates a new Microsoft Access Workspace object and appends it to the **Workspaces** collection. It then enumerates the **Workspaces** collections and the **Properties** collection of the **Workspace** object.</span></span>

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

<span data-ttu-id="a775f-p106">En este ejemplo, se usa el método **CreateWorkspace** para crear un área de trabajo de Microsoft Access. A continuación, se enumeran las propiedades del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="a775f-p106">This example uses the **CreateWorkspace** method to create a Microsoft Access workspace. It then lists the properties of theworkspace.</span></span>

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

