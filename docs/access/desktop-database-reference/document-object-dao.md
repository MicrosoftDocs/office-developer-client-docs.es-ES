---
title: Objeto Document (DAO)
TOCTitle: Document Object
ms:assetid: b51d4545-b157-4c7c-fdbe-16a25afffdb3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822082(v=office.15)
ms:contentKeyID: 48547247
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4dbd7de05a3bb2402d436e4bbac59f1ca4687317
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026333"
---
# <a name="document-object-dao"></a><span data-ttu-id="a3842-102">Objeto Document (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3842-102">Document object (DAO)</span></span>

<span data-ttu-id="a3842-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3842-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3842-p101">Un objeto **Document** incluye información sobre una instancia de un objeto. El objeto puede ser una base de datos, una tabla guardada, una consulta o una relación (sólo bases de datos del motor de base de datos de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a3842-p101">A **Document** object includes information about one instance of an object. The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3842-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3842-106">Remarks</span></span>

<span data-ttu-id="a3842-p102">Cada objeto **Container** tiene una colección **Documents** que contiene objetos **Document** que describen instancias de objetos integrados del tipo especificado por el objeto **Container**. La tabla siguiente enumera el tipo de cada objeto **Document**, el nombre de su objeto **Container** y el tipo de información que contiene **Document**.</span><span class="sxs-lookup"><span data-stu-id="a3842-p102">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. The following table lists the type of object each **Document** describes, the name of its **Container** object, and what type of information **Document** contains.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3842-109">Documento</span><span class="sxs-lookup"><span data-stu-id="a3842-109">Document</span></span></p></th>
<th><p><span data-ttu-id="a3842-110">Contenedor</span><span class="sxs-lookup"><span data-stu-id="a3842-110">Container</span></span></p></th>
<th><p><span data-ttu-id="a3842-111">Contiene información sobre</span><span class="sxs-lookup"><span data-stu-id="a3842-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3842-112">Base de datos</span><span class="sxs-lookup"><span data-stu-id="a3842-112">Database</span></span></p></td>
<td><p><span data-ttu-id="a3842-113">Bases de datos</span><span class="sxs-lookup"><span data-stu-id="a3842-113">Databases</span></span></p></td>
<td><p><span data-ttu-id="a3842-114">Bases de datos guardadas</span><span class="sxs-lookup"><span data-stu-id="a3842-114">Saved database</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3842-115">Tabla o consulta</span><span class="sxs-lookup"><span data-stu-id="a3842-115">Table or query</span></span></p></td>
<td><p><span data-ttu-id="a3842-116">Tablas</span><span class="sxs-lookup"><span data-stu-id="a3842-116">Tables</span></span></p></td>
<td><p><span data-ttu-id="a3842-117">Tabla o consulta guardada</span><span class="sxs-lookup"><span data-stu-id="a3842-117">Saved table or query</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3842-118">Relación</span><span class="sxs-lookup"><span data-stu-id="a3842-118">Relationship</span></span></p></td>
<td><p><span data-ttu-id="a3842-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a3842-119">Relations</span></span></p></td>
<td><p><span data-ttu-id="a3842-120">Relación guardada</span><span class="sxs-lookup"><span data-stu-id="a3842-120">Saved relationship</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a3842-p103">[!NOTA] No confunda los objetos **Container** enumerados en la tabla anterior con las colecciones del mismo nombre. El objeto **Container** de bases de datos hace referencia a todos los objetos de bases de datos guardados pero la colección **Databases** hace referencia sólo a los objetos de bases de datos que están abiertos en un área de trabajo en particular.</span><span class="sxs-lookup"><span data-stu-id="a3842-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="a3842-123">Con un objeto **Document**, puede:</span><span class="sxs-lookup"><span data-stu-id="a3842-123">With a **Document** object, you can:</span></span>

- <span data-ttu-id="a3842-124">Utilizar la propiedad **Name** para devolver el nombre que un usuario o el motor de base de datos de Microsoft Access dieron al objeto cuando se creó.</span><span class="sxs-lookup"><span data-stu-id="a3842-124">Use the **Name** property to return the name that a user or the Microsoft Access database engine gave to the object when it was created.</span></span>

- <span data-ttu-id="a3842-125">Usar la propiedad **Container** para devolver el nombre del objeto **Container** que contiene el objeto **Document**.</span><span class="sxs-lookup"><span data-stu-id="a3842-125">Use the **Container** property to return the name of the **Container** object that contains the **Document** object.</span></span>

- <span data-ttu-id="a3842-p104">Utilizar la propiedad **Owner** para establecer o devolver la propiedad del objeto. Para configurar la propiedad **Owner**, debe tener permiso de escritura para el objeto **Document** y establecer la propiedad en el nombre de un objeto **User** o **Group** existente.</span><span class="sxs-lookup"><span data-stu-id="a3842-p104">Use the **Owner** property to set or return the owner of the object. To set the **Owner** property, you must have write permission for the **Document** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="a3842-p105">Usar las propiedades **UserName** o **Permissions** para establecer o devolver los permisos de acceso para un usuario o grupo para el objeto. Para configurar estas propiedades, debe tener permiso de escritura para el objeto **Document** y establecer la propiedad **UserName** en el nombre de un objeto **User** o **Group** existente.</span><span class="sxs-lookup"><span data-stu-id="a3842-p105">Use the **UserName** or **Permissions** properties to set or return the access permissions of a user or group for the object. To set these properties, you must have write permission for the **Document** object, and you must set the **UserName** property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="a3842-130">Utilizar las propiedades **DateCreated** y **LastUpdated** para devolver la fecha y hora en que se creó y modificó por última vez el objeto **Document**.</span><span class="sxs-lookup"><span data-stu-id="a3842-130">Use the **DateCreated** and **LastUpdated** properties to return the date and time when the **Document** object was created and last modified.</span></span>

<span data-ttu-id="a3842-p106">Dado que un objeto **Document** corresponde a un objeto existente, no se pueden crear nuevos objetos **Document** o eliminar los existentes. Para hacer referencia a un objeto **Document** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3842-p106">Because a **Document** object corresponds to an existing object, you can't create new **Document** objects or delete existing ones. To refer to a **Document** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="a3842-133">**Documents**(0)</span><span class="sxs-lookup"><span data-stu-id="a3842-133">**Documents**(0)</span></span>

- <span data-ttu-id="a3842-134">**Documentos** ("*nombre*")</span><span class="sxs-lookup"><span data-stu-id="a3842-134">**Documents**("*name*")</span></span>

- <span data-ttu-id="a3842-135">**Documentos**\!\[*nombre*\]</span><span class="sxs-lookup"><span data-stu-id="a3842-135">**Documents**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="a3842-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a3842-136">Example</span></span>

<span data-ttu-id="a3842-137">En este ejemplo se enumera la colección **Documents** del contenedor Tables y, a continuación, se enumera la colección **Properties** del primer objeto **Document** de la colección.</span><span class="sxs-lookup"><span data-stu-id="a3842-137">This example enumerates the **Documents** collection of the Tables container, and then enumerates the **Properties** collection of the first **Document** object in the collection.</span></span>

```vb 
Sub DocumentX() 
 
 Dim dbsNorthwind As Database 
 Dim docLoop As Document 
 Dim prpLoop As Property 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind.Containers!Tables 
 Debug.Print "Documents in " & .Name & " container" 
 ' Enumerate the Documents collection of the Tables 
 ' container. 
 For Each docLoop In .Documents 
 Debug.Print " " & docLoop.Name 
 Next docLoop 
 With .Documents(0) 
 ' Enumerate the Properties collection of the first. 
 ' Document object of the Tables container. 
 Debug.Print "Properties of " & .Name & " document" 
 On Error Resume Next 
 For Each prpLoop In .Properties 
 Debug.Print " " & prpLoop.Name & " = " & _ 
 prpLoop 
 Next prpLoop 
 On Error GoTo 0 
 End With 
 End With 
 
 dbsNorthwind.Close 
 
End Sub 
 
```

<br/>

<span data-ttu-id="a3842-138">En este ejemplo se utilizan las propiedades **Owner** y **SystemDB** para mostrar los propietarios de varios objetos **Document**.</span><span class="sxs-lookup"><span data-stu-id="a3842-138">This example uses the **Owner** and **SystemDB** properties to show the owners of a variety of **Document** objects.</span></span>

```vb 
Sub OwnerX() 
 
 ' Ensure that the Microsoft Access workgroup file is 
 ' available. 
 DBEngine.SystemDB = "system.mdw" 
 
 Dim dbsNorthwind As Database 
 Dim ctrLoop As Container 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 Debug.Print "Document owners:" 
 ' Enumerate Containers collection and show the owner 
 ' of the first Document in each container's Documents 
 ' collection. 
 For Each ctrLoop In .Containers 
 With ctrLoop 
 Debug.Print " [" & .Documents(0).Name & _ 
 "] in [" & .Name & _ 
 "] container owned by [" & _ 
 .Documents(0).Owner & "]" 
 End With 
 Next ctrLoop 
 
 .Close 
 End With 
 
End Sub 
 
```

