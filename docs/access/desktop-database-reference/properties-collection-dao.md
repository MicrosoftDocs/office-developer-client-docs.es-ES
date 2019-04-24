---
title: Colección Properties (DAO)
TOCTitle: Properties collection
ms:assetid: cd07184a-a261-29c9-542f-bc2eff6f4af6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834455(v=office.15)
ms:contentKeyID: 48547753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 515d28f0d7d99359c36df79cf3b8769d8f71e06d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301284"
---
# <a name="properties-collection-dao"></a><span data-ttu-id="57bc3-102">Colección Properties (DAO)</span><span class="sxs-lookup"><span data-stu-id="57bc3-102">Properties collection (DAO)</span></span>

<span data-ttu-id="57bc3-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57bc3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57bc3-104">Una colección **Properties** contiene todos los objetos **[Property](property-object-dao.md)** de una instancia específica de un objeto.</span><span class="sxs-lookup"><span data-stu-id="57bc3-104">A **Properties** collection contains all the **[Property](property-object-dao.md)** objects for a specific instance of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="57bc3-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="57bc3-105">Remarks</span></span>

<span data-ttu-id="57bc3-p101">Todos los objetos DAO, salvo los objetos **Connection** y **Error**, contienen una colección **Properties**, que tiene varios objetos **Property** integrados. Estos objetos **Property** (que a menudo se denominan propiedades) caracterizan de manera única esa instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="57bc3-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection, which has certain built-in **Property** objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="57bc3-p102">Además de las propiedades integradas, también puede crear y agregar sus propias propiedades definidas por el usuario. Para agregar una propiedad definida por el usuario a una instancia existente de un objeto, primero debe definir sus características con el método **CreateProperty** y después agregarla a la colección con el método **Append**. Si se hace referencia a un objeto **Property** definido por el usuario que aún no ha sido anexado a una colección **Properties**, se producirá un error, y lo mismo ocurre al anexar un objeto **Property** definido por el usuario a una colección **Properties** que contiene un objeto **Property** del mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="57bc3-p102">In addition to the built-in properties, you can also create and add your own user-defined properties. To add a user-defined property to an existing instance of an object, first define its characteristics with the **CreateProperty** method, then add it to the collection with the **Append** method. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="57bc3-111">Puede utilizar el método **Delete** para quitar propiedades definidas por el usuario de la colección **Properties**, pero no puede quitar propiedades integradas.</span><span class="sxs-lookup"><span data-stu-id="57bc3-111">You can use the **Delete** method to remove user-defined properties from the **Properties** collection, but you can't remove built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="57bc3-p103">[!NOTA] Un objeto **Property** definido por el usuario sólo está asociado con la instancia concreta de un objeto. La propiedad no está definida para todas las instancias de objetos del tipo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="57bc3-p103">A user-defined **Property** object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="57bc3-114">Para hacer referencia a un objeto **Property** integrado en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="57bc3-114">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="57bc3-115">DataObject. **Propiedades** de comprendi</span><span class="sxs-lookup"><span data-stu-id="57bc3-115">object.**Properties**(0)</span></span>

- <span data-ttu-id="57bc3-116">DataObject. **Propiedades** de ("nombre")</span><span class="sxs-lookup"><span data-stu-id="57bc3-116">object.**Properties**("name")</span></span>

- <span data-ttu-id="57bc3-117">DataObject. **Propiedades** de \! \[nombre de\]</span><span class="sxs-lookup"><span data-stu-id="57bc3-117">object.**Properties**\!\[name\]</span></span>

<span data-ttu-id="57bc3-118">Para una propiedad integrada, también se puede usar la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="57bc3-118">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="57bc3-119">Object.Name</span><span class="sxs-lookup"><span data-stu-id="57bc3-119">object.name</span></span>

> [!NOTE]
> <span data-ttu-id="57bc3-120">Para una propiedad definida por el usuario, debe usar el objeto completo. **Propiedades** de ("nombre") sintaxis.</span><span class="sxs-lookup"><span data-stu-id="57bc3-120">For a user-defined property, you must use the full object.**Properties**("name") syntax.</span></span>

<span data-ttu-id="57bc3-p104">Con los mismos formatos de sintaxis, también se puede hacer referencia a la propiedad **Value** de un objeto **Property**. El contexto de la referencia determinará si se está haciendo referencia al objeto **Property** en sí o a la propiedad **Value** del objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="57bc3-p104">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

## <a name="example"></a><span data-ttu-id="57bc3-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="57bc3-123">Example</span></span>

<span data-ttu-id="57bc3-p105">En este ejemplo se crea una propiedad definida por el usuario para la base de datos actual, se establecen sus propiedades **Type** y **Value** y se agrega a la colección **Properties** de la base de datos. A continuación, se enumeran todas las propiedades de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="57bc3-p105">This example creates a user-defined property for the current database, sets its **Type** and **Value** properties, and appends it to the **Properties** collection of the database. Then the example enumerates all properties in the database.</span></span>

```vb
    Sub PropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpNew As Property 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Create and append user-defined property. 
     Set prpNew = .CreateProperty() 
     prpNew.Name = "UserDefined" 
     prpNew.Type = dbText 
     prpNew.Value = "This is a user-defined property." 
     .Properties.Append prpNew 
     
     ' Enumerate all properties of current database. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     With prpLoop 
     Debug.Print " " & .Name 
     Debug.Print " Type: " & .Type 
     Debug.Print " Value: " & .Value 
     Debug.Print " Inherited: " & _ 
     .Inherited 
     End With 
     Next prpLoop 
     
     ' Delete new property because this is a 
     ' demonstration. 
     .Properties.Delete "UserDefined" 
     End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="57bc3-p106">En este ejemplo se intenta establecer el valor de una propiedad definida por el usuario. Si la propiedad no existe, se utiliza el método **CreateProperty** para crear y definir el valor de la nueva propiedad. Se requiere el procedimiento SetProperty para que pueda ejecutarse este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="57bc3-p106">This example tries to set the value of a user-defined property. If the property doesn't exist, it uses the **CreateProperty** method to create and set the value of the new property. The SetProperty procedure is required for this procedure to run.</span></span>

```vb
    Sub CreatePropertyX() 
     
     Dim dbsNorthwind As Database 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Set the Archive property to True. 
     SetProperty dbsNorthwind, "Archive", True 
     
     With dbsNorthwind 
     Debug.Print "Properties of " & .Name 
     
     ' Enumerate Properties collection of the Northwind 
     ' database. 
     For Each prpLoop In .Properties 
     If prpLoop <> "" Then Debug.Print " " & _ 
     prpLoop.Name & " = " & prpLoop 
     Next prpLoop 
     
     ' Delete the new property since this is a 
     ' demonstration. 
     .Properties.Delete "Archive" 
     
     .Close 
     End With 
     
    End Sub 
     
    Sub SetProperty(dbsTemp As Database, strName As String, _ 
     booTemp As Boolean) 
     
     Dim prpNew As Property 
     Dim errLoop As Error 
     
     ' Attempt to set the specified property. 
     On Error GoTo Err_Property 
     dbsTemp.Properties("strName") = booTemp 
     On Error GoTo 0 
     
     Exit Sub 
     
    Err_Property: 
     
     ' Error 3270 means that the property was not found. 
     If DBEngine.Errors(0).Number = 3270 Then 
     ' Create property, set its value, and append it to the 
     ' Properties collection. 
     Set prpNew = dbsTemp.CreateProperty(strName, _ 
     dbBoolean, booTemp) 
     dbsTemp.Properties.Append prpNew 
     Resume Next 
     Else 
     ' If different error has occurred, display message. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & vbCr & _ 
     errLoop.Description 
     Next errLoop 
     End 
     End If 
     
    End Sub
```
