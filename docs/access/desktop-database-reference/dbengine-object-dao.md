---
title: DBEngine Object (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc2889ad38bdc95316735901b25314f26d8df754
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486227"
---
# <a name="dbengine-object-dao"></a><span data-ttu-id="2a7d3-102">DBEngine Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="2a7d3-102">DBEngine Object (DAO)</span></span>

<span data-ttu-id="2a7d3-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a7d3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a7d3-104">El objeto **DBEngine** es el objeto de nivel superior en el modelo de objetos DAO.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-104">The **DBEngine** object is the top level object in the DAO object model.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a7d3-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a7d3-105">Remarks</span></span>

<span data-ttu-id="2a7d3-p101">El objeto **DBEngine** contiene y controla todos los demás objetos de la jerarquía de objetos DAO. No puede crear objetos **DBEngine** adicionales y el objeto **DBEngine** no es un elemento de ninguna colección.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-p101">The **DBEngine** object contains and controls all other objects in the hierarchy of DAO objects. You can't create additional **DBEngine** objects, and the **DBEngine** object isn't an element of any collection.</span></span>

<span data-ttu-id="2a7d3-108">Con cualquier tipo de base de datos o conexión puede:</span><span class="sxs-lookup"><span data-stu-id="2a7d3-108">With any type of database or connection, you can:</span></span>

  - <span data-ttu-id="2a7d3-109">Utilizar la propiedad **Version** para obtener el número de versión DAO.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-109">Use the **Version** property to obtain the DAO version number.</span></span>

  - <span data-ttu-id="2a7d3-110">Usar la propiedad **LoginTimeout** para obtener o establecer el tiempo de espera de inicio de sesión de ODBC y el método **RegisterDatabase** para proporcionar información de ODBC al motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-110">Use the **LoginTimeout** property to obtain or set the ODBC login timeout, and the **RegisterDatabase** method to provide ODBC information to the Microsoft Access database engine.</span></span>

  - <span data-ttu-id="2a7d3-111">Usar las propiedades **DefaultPassword** y **DefaultUser** a fin de establecer la identificación de usuario y la contraseña para el objeto **Workspace** predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-111">Use the **DefaultPassword** and **DefaultUser** properties to set the user identification and password for the default **Workspace** object.</span></span>

  - <span data-ttu-id="2a7d3-p102">Utilizar el método **CreateWorkspace** para crear un nuevo objeto **Workspace**. Puede emplear argumentos opcionales para anular la configuración de las propiedades **DefaultType**, **DefaultPassword** y **DefaultUser**.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-p102">Use the **CreateWorkspace** method to create a new **Workspace** object. You can use optional arguments to override the settings of the **DefaultType**, **DefaultPassword**, and **DefaultUser** properties.</span></span>

  - <span data-ttu-id="2a7d3-114">Usar el método **OpenDatabase** para abrir una base de datos en el objeto **Workspace** predeterminado y utilizar los métodos **BeginTrans**, **Commit** y **Rollback** para controlar las transacciones en el objeto **Workspace** predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-114">Use the **OpenDatabase** method to open a database in the default **Workspace**, and use the **BeginTrans**, **Commit**, and **Rollback** methods to control transactions on the default **Workspace**.</span></span>

  - <span data-ttu-id="2a7d3-115">Utilizar la colección **Workspaces** para hacer referencia a objetos **Workspace** específicos.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-115">Use the **Workspaces** collection to reference specific **Workspace** objects.</span></span>

  - <span data-ttu-id="2a7d3-116">Usar la colección **Errors** para examinar los detalles de errores de acceso a datos.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-116">Use the **Errors** collection to examine data access error details.</span></span>

<span data-ttu-id="2a7d3-p103">Otras propiedades y métodos sólo están disponibles cuando utiliza DAO con el motor de base de datos de Microsoft Access. Puede utilizarlos para controlar el motor de base de datos de Microsoft Access, modificar sus propiedades y realizar tareas en objetos temporales que no son elementos de colecciones. Por ejemplo, puede:</span><span class="sxs-lookup"><span data-stu-id="2a7d3-p103">Other properties and methods are only available when you use DAO with the Microsoft Access database engine. You can use them to control the Microsoft Access database engine, manipulate its properties, and perform tasks on temporary objects that aren't elements of collections. For example, you can:</span></span>

  - <span data-ttu-id="2a7d3-120">Utilizar el método **CreateDatabase** para crear un nuevo objeto **Database** del motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-120">Use the **CreateDatabase** method to create a new Microsoft Access database engine **Database** object.</span></span>

  - <span data-ttu-id="2a7d3-121">Usar el método **Idle** para que el motor de base de datos de Microsoft Access pueda completar todas las tareas pendientes.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-121">Use the **Idle** method to enable the Microsoft Access database engine to complete any pending tasks.</span></span>

  - <span data-ttu-id="2a7d3-122">Utilizar los métodos **CompactDatabase** y **RepairDatabase** para mantener los archivos de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-122">Use the **CompactDatabase** and **RepairDatabase** methods to maintain database files.</span></span>

  - <span data-ttu-id="2a7d3-p104">Usar las propiedades **IniPath** y **SystemDB** para especificar la ubicación de la información del Registro de Windows para el motor de base de datos de Microsoft Access y el archivo de información de grupo de trabajo de Microsoft Access respectivamente. El método **SetOption** le permite anular la configuración del Registro de Windows para el motor de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-p104">Use the **IniPath** and **SystemDB** properties to specify the location of Microsoft Access database engine Windows Registry information and the Microsoft Access workgroup information file, respectively. The **SetOption** method allows you override windows registry settings for the Microsoft Access database engine.</span></span>

<span data-ttu-id="2a7d3-125">Una vez modificados los valores de las propiedades **DefaultType** y **IniPath**, sólo los objetos **Workspace** posteriores reflejarán estos cambios.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-125">After you change the **DefaultType** and **IniPath** property settings, only subsequent **Workspace** objects will reflect these changes.</span></span>

<span data-ttu-id="2a7d3-126">Para hacer referencia a una colección que pertenece al objeto **DBEngine**, o a un método o propiedad que se aplica a este objeto, utilice la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a7d3-126">To refer to a collection that belongs to the **DBEngine** object, or to refer to a method or property that applies to this object, use this syntax:</span></span>

<span data-ttu-id="2a7d3-127">\[**DBEngine**. \] \[colección | método | (propiedad)\]</span><span class="sxs-lookup"><span data-stu-id="2a7d3-127">\[**DBEngine**.\]\[collection | method | property\]</span></span>

## <a name="example"></a><span data-ttu-id="2a7d3-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a7d3-128">Example</span></span>

<span data-ttu-id="2a7d3-129">En este ejemplo se enumeran las colecciones del objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="2a7d3-129">This example enumerates the collections of the **DBEngine** object.</span></span>

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
