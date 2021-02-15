---
title: Fields (colección)
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce08ac5952151471ce74afd9a8a49600d8e8f633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314136"
---
# <a name="fields-collection"></a><span data-ttu-id="3ec2a-102">Fields (colección)</span><span class="sxs-lookup"><span data-stu-id="3ec2a-102">Fields collection</span></span>


<span data-ttu-id="3ec2a-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ec2a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ec2a-p101">La colección **Fields** es una de las colecciones intrínsecas de ADO. Una colección es un conjunto ordenado de elementos a los que se puede hacer referencia como unidad.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p101">The **Fields** collection is one of ADO's intrinsic collections. A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="3ec2a-p102">La colección **Fields** contiene un objeto **Field** para cada campo (columna) del **conjunto de registros**. Igual que todas las colecciones de ADO, tiene las propiedades **Count** e **Item**, así como los métodos **Append** y **Refresh**. También tiene los métodos **CancelUpdate**, **Delete**, **Resync** y **Update**, que no están disponibles para otras colecciones de ADO.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p102">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**. Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods. It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="3ec2a-109">Examinar la colección Fields</span><span class="sxs-lookup"><span data-stu-id="3ec2a-109">Examining the Fields Collection</span></span>

<span data-ttu-id="3ec2a-p103">Considere la colección **Fields** del **conjunto de registros** de ejemplo que se introdujo en este capítulo. El **conjunto de registros** de ejemplo se derivó de la instrucción SQL:</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p103">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter. The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="3ec2a-112">Por tanto, se deberían observar tres campos en la colección **Fields** del **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

<span data-ttu-id="3ec2a-p104">Este código simplemente determina el número de objetos **Field** que contiene la colección **Fields** utilizando la propiedad **Contar** y recorre en bucle la colección, para devolver el valor de la propiedad **Name** para cada objeto **Field**. Se pueden utilizar muchas más propiedades de **campo** para obtener información acerca de un campo. Para obtener más información acerca de las consultas en un **campo**, vea [El objeto Field](the-field-object.md).</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p104">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object. You can use many more **Field** properties to get information about a field. For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="3ec2a-116">Contar columnas</span><span class="sxs-lookup"><span data-stu-id="3ec2a-116">Counting Columns</span></span>

<span data-ttu-id="3ec2a-p105">Como cabe esperar, la propiedad **Contar** devuelve la cantidad real de objetos **Field** contenidos en la colección **Fields**. Dado que la numeración de elementos de una colección empieza por cero, los bucles siempre se deben codificar a partir del elemento cero y hasta el valor de la propiedad **Contar** menos 1. Si se utiliza Microsoft Visual Basic y se desea recorrer en bucle los elementos de una colección sin comprobar la propiedad **Contar**, use el comando **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p105">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection. Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="3ec2a-120">Si la propiedad **Count** es cero, significa que no hay ningún objeto en la colección.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="3ec2a-121">Obtener el campo</span><span class="sxs-lookup"><span data-stu-id="3ec2a-121">Getting to the Field</span></span>

<span data-ttu-id="3ec2a-p106">Al igual que ocurre con cualquier colección de ADO, la propiedad **Item** es la predeterminada de la colección. Devuelve el objeto **Field** individual especificado por el nombre o el índice que se le pasa. Por tanto, las instrucciones siguientes son equivalentes para el **conjunto de registros** de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p106">As with any ADO collection, the **Item** property is the default property of the collection. It returns the individual **Field** object specified by the name or index passed to it. Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="3ec2a-p107">Si estos métodos son equivalentes, ¿cuál es el mejor? Depende. El uso de un índice para recuperar un **campo** de la colección es más rápido porque obtiene acceso al **campo** directamente, sin tener que realizar una búsqueda en cadenas. Por otra parte, se debe conocer el orden de los **campos** dentro de la colección y, si cambia el orden, se tendrá que cambiar la referencia al índice del **campo** siempre que aparezca. Aunque es un método un poco más lento, el uso del nombre del **campo** es más flexible porque no depende del orden de los **campos** en la colección.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p107">If these methods are equivalent, which is best? It depends. Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup. On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs. Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="3ec2a-130">Utilizar el método Refresh</span><span class="sxs-lookup"><span data-stu-id="3ec2a-130">Using the Refresh Method</span></span>

<span data-ttu-id="3ec2a-p108">Al contrario que en otras colecciones de ADO, el uso del método **Refresh** con la colección **Fields** no tiene efectos visibles. Para recuperar cambios de la estructura de la base de datos subyacente, se debe usar el método **Requery** o, si el objeto **Recordset** no admite marcadores, el método **MoveFirst**, que provocará que se ejecute otra vez el comando para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p108">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="3ec2a-133">Agregar campos a un conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="3ec2a-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="3ec2a-134">El método **Append** se utiliza para agregar campos a un **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="3ec2a-p109">El método **Append** se puede utilizar para fabricar un **conjunto de registros** mediante programación sin abrir una conexión con un origen de datos. Si se llama al método **Append** en la colección **Fields** de un **conjunto de registros** abierto o en un **conjunto de registros** donde se ha configurado la propiedad **ActiveConnection**, se producirá un error en tiempo de ejecución. Sólo se pueden anexar campos a un **conjunto de registros** que no esté abierto y que aún no se haya conectado a un origen de datos. No obstante, para especificar valores para los **campos** recién anexados, primero se debe abrir el **conjunto de registros**.</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p109">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source. A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set. You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source. However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="3ec2a-p110">Con frecuencia, los programadores necesitan una ubicación para almacenar temporalmente algunos datos, o desean que ciertos datos se comporten como si procediesen de un servidor, para que puedan participar en enlaces de datos en una interfaz de usuario. ADO (junto con el [servicio de cursores de Microsoft para OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) permite al programador crear un objeto **Recordset** vacío especificando información de columnas y llamando a **Open**. En el siguiente ejemplo, se anexan tres nuevos campos a un nuevo objeto **Recordset**. A continuación, se abre el **conjunto de registros**, se agregan dos nuevos registros y se conserva el **conjunto de registros** en un archivo (para obtener más información acerca de la persistencia de **conjuntos de registros**, vea el [Capítulo 5: Actualizar y almacenar datos](chapter-5-updating-and-persisting-data.md)).</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p110">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface. ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**. In the following example, three new fields are appended to a new **Recordset** object. Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file. (For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

<span data-ttu-id="3ec2a-p111">El uso del método **Append** de **Fields** difiere entre el objeto **Recordset** y el objeto **Record**. Para obtener más información acerca del objeto **Record**, vea el [Capítulo 10: Objetos Record y Stream](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="3ec2a-p111">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object. For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

