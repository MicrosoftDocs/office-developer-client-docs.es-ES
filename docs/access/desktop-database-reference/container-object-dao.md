---
title: Objeto contenedor (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295635"
---
# <a name="container-object-dao"></a><span data-ttu-id="efbe0-102">Objeto contenedor (DAO)</span><span class="sxs-lookup"><span data-stu-id="efbe0-102">Container object (DAO)</span></span>

<span data-ttu-id="efbe0-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="efbe0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="efbe0-104">Un objeto **Container** agrupa juntos tipos similares de objetos **Document**.</span><span class="sxs-lookup"><span data-stu-id="efbe0-104">A **Container** object groups similar types of **Document** objects together.</span></span>

## <a name="remarks"></a><span data-ttu-id="efbe0-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efbe0-105">Remarks</span></span>

<span data-ttu-id="efbe0-p101">Cada objeto **Database** tiene una colección **Containers** que consta de objetos **Container** integrados. Las aplicaciones pueden definir sus propios tipos de documentos y contenedores correspondientes (sólo bases de datos del motor de base de datos de Microsoft Access); no obstante, es posible que no se admitan siempre estos objetos a través de DAO.</span><span class="sxs-lookup"><span data-stu-id="efbe0-p101">Each **Database** object has a **Containers** collection consisting of built-in **Container** objects. Applications can define their own document types and corresponding containers (Microsoft Access database engine databases only); however, these objects may not always be supported through DAO.</span></span>

<span data-ttu-id="efbe0-p102">Algunos de estos objetos **Container** están definidos por el motor de base de datos de Microsoft Access mientras que otros pueden estar definidos por otras aplicaciones. La tabla siguiente enumera el nombre de cada objeto **Container** definido por el motor de base de datos de Microsoft Access y el tipo de información que contiene.</span><span class="sxs-lookup"><span data-stu-id="efbe0-p102">Some of these **Container** objects are defined by the Microsoft Access database engine while others may be defined by other applications. The following table lists the name of each **Container** object defined by the Microsoft Access database engine and what type of information it contains.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="efbe0-110">Nombre del contenedor</span><span class="sxs-lookup"><span data-stu-id="efbe0-110">Container name</span></span></p></th>
<th><p><span data-ttu-id="efbe0-111">Contiene información sobre</span><span class="sxs-lookup"><span data-stu-id="efbe0-111">Contains information about</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="efbe0-112">Databases</span><span class="sxs-lookup"><span data-stu-id="efbe0-112">Databases</span></span></p></td>
<td><p><span data-ttu-id="efbe0-113">Bases de datos guardadas</span><span class="sxs-lookup"><span data-stu-id="efbe0-113">Saved databases</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="efbe0-114">Tablas</span><span class="sxs-lookup"><span data-stu-id="efbe0-114">Tables</span></span></p></td>
<td><p><span data-ttu-id="efbe0-115">Tablas y consultas guardadas</span><span class="sxs-lookup"><span data-stu-id="efbe0-115">Saved tables and queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="efbe0-116">Relations</span><span class="sxs-lookup"><span data-stu-id="efbe0-116">Relations</span></span></p></td>
<td><p><span data-ttu-id="efbe0-117">Relaciones guardadas</span><span class="sxs-lookup"><span data-stu-id="efbe0-117">Saved relationships</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="efbe0-p103">[!NOTA] No confunda los objetos **Container** enumerados en la tabla anterior con las colecciones del mismo nombre. El objeto **Container** de bases de datos hace referencia a todos los objetos de bases de datos guardados pero la colección **Databases** hace referencia sólo a los objetos de bases de datos que están abiertos en un área de trabajo en particular.</span><span class="sxs-lookup"><span data-stu-id="efbe0-p103">Don't confuse the **Container** objects listed in the preceding table with the collections of the same name. The Databases **Container** object refers to all saved database objects, but the **Databases** collection refers only to database objects that are open in a particular workspace.</span></span>

<span data-ttu-id="efbe0-p104">Cada objeto **Container** tiene una colección **Documents** que contiene objetos **Document** que describen instancias de objetos integrados del tipo especificado por el objeto **Container**. Normalmente, utiliza un objeto **Container** como vínculo intermediario para la información del objeto **Document**. Puede utilizar igualmente la colección **Containers** para establecer una seguridad para todos los objetos **Document** de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="efbe0-p104">Each **Container** object has a **Documents** collection containing **Document** objects that describe instances of built-in objects of the type specified by the **Container**. You typically use a **Container** object as an intermediate link to the information in the **Document** object. You can also use the **Containers** collection to set security for all **Document** objects of a given type.</span></span>

<span data-ttu-id="efbe0-123">Con un objeto **Container** existente, puede:</span><span class="sxs-lookup"><span data-stu-id="efbe0-123">With an existing **Container** object, you can:</span></span>

- <span data-ttu-id="efbe0-124">Utilizar la propiedad **Name** para devolver el nombre predefinido del objeto **Container**.</span><span class="sxs-lookup"><span data-stu-id="efbe0-124">Use the **Name** property to return the predefined name of the **Container** object.</span></span>

- <span data-ttu-id="efbe0-p105">Utilizar la propiedad **Owner** para establecer o devolver el propietario del objeto **Container**. Para establecer la propiedad **Owner**, debe tener permiso de escritura para el objeto **Container** y establecer la propiedad en el nombre de un objeto **User** o **Group** existente.</span><span class="sxs-lookup"><span data-stu-id="efbe0-p105">Use the **Owner** property to set or return the owner of the **Container** object. To set the **Owner** property, you must have write permission for the **Container** object, and you must set the property to the name of an existing **User** or **Group** object.</span></span>

- <span data-ttu-id="efbe0-127">Utilizar las propiedades **Permissions** y **UserName** para establecer permisos de acceso para el objeto **Container**; cualquier objeto **Document** creado en la colección **Documents** de un objeto **Container** hereda estos valores de permisos de acceso.</span><span class="sxs-lookup"><span data-stu-id="efbe0-127">Use the **Permissions** and **UserName** properties to set access permissions for the **Container** object; any **Document** object created in the **Documents** collection of a **Container** object inherits these access permission settings.</span></span>

<span data-ttu-id="efbe0-128">Como los objetos **Container** están integrados, no puede crear nuevos objetos **Container** o eliminar los existentes.</span><span class="sxs-lookup"><span data-stu-id="efbe0-128">Because **Container** objects are built-in, you can't create new **Container** objects or delete existing ones.</span></span>

<span data-ttu-id="efbe0-129">Para hacer referencia a un objeto **Container** en una colección mediante su número ordinal o mediante el valor de la propiedad **Name**, utilice una de las formas sintácticas siguientes:</span><span class="sxs-lookup"><span data-stu-id="efbe0-129">To refer to a **Container** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="efbe0-130">**Contenedores**(0)</span><span class="sxs-lookup"><span data-stu-id="efbe0-130">**Containers**(0)</span></span>

- <span data-ttu-id="efbe0-131">**Contenedores**("*nombre*")</span><span class="sxs-lookup"><span data-stu-id="efbe0-131">**Containers**("*name*")</span></span>

- <span data-ttu-id="efbe0-132">**Contenedores** \! \[ *name*\]</span><span class="sxs-lookup"><span data-stu-id="efbe0-132">**Containers**\!\[*name*\]</span></span>

## <a name="example"></a><span data-ttu-id="efbe0-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="efbe0-133">Example</span></span>

<span data-ttu-id="efbe0-134">En este ejemplo se enumera la colección **Containers** de la base de datos Northwind y la colección **Properties** de cada objeto **Container** de la colección.</span><span class="sxs-lookup"><span data-stu-id="efbe0-134">This example enumerates the **Containers** collection of the Northwind database and the **Properties** collection of each **Container** object in the collection.</span></span>

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
