---
title: Agregar datos a un conjunto de registros
TOCTitle: Adding data to a Recordset
ms:assetid: a3d121a8-f52f-66cd-8849-c3a75aeb276a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249761(v=office.15)
ms:contentKeyID: 48546797
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d16eb5871bfe55af58a89cc06b413e8404df8cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701399"
---
# <a name="adding-data-to-a-recordset"></a><span data-ttu-id="60347-102">Agregar datos a un conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="60347-102">Adding data to a Recordset</span></span>

<span data-ttu-id="60347-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60347-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60347-p101">Probablemente, el objeto **Recordset** es el más usado de los objetos de ADO. En ADO, un **conjunto de registros** se entiende mejor como la combinación de un conjunto de resultados de un origen de datos y sus comportamientos de cursor asociados. Así pues, puede colocar datos en un **conjunto de registros** y luego utilizar los métodos y las propiedades del **conjunto de registros** para desplazarse por las filas de datos, ver los valores de las filas y manipular de otras maneras el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="60347-p101">The **Recordset** is probably the most used of the ADO objects. In ADO a **Recordset** is best thought of as the combination of a result set from a data source and its associated cursor behaviors. Thus, you can put data into a **Recordset** and then use the **Recordset** methods and properties to navigate through the rows of data, view the values in the rows, and otherwise manipulate the result set.</span></span>

<span data-ttu-id="60347-p102">Esta sección se centra en agregar datos al objeto **Recordset**. Para obtener información acerca de la navegación por los datos o la actualización de los datos, vea el [Capítulo 4: Modificar datos](chapter-4-editing-data.md) y el [Capítulo 5: Actualizar y almacenar datos](chapter-5-updating-and-persisting-data.md). No siempre son necesarias las características avanzadas de un objeto **Command** para agregar un conjunto de resultados a un objeto **Recordset**. A menudo, se puede ejecutar el comando si establece la propiedad **Origen** para el objeto **Recordset** o pasa una cadena de comandos al método **Open** del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="60347-p102">This section will focus on adding data to the **Recordset**. For information about navigating through the data or updating the data, see [Chapter 4: Editing Data](chapter-4-editing-data.md) and [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md). You do not always need the advanced capabilities of a **Command** object to add your result set to a **Recordset**. Often, you can execute your command by setting the **Source** property on the **Recordset** or passing a command string to the **Recordset** object **Open** method.</span></span>

<span data-ttu-id="60347-p103">Hay diversas formas de agregar datos a un **conjunto de registros** desde un origen de datos. La técnica que se utilice depende de las necesidades de la aplicación y de las características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="60347-p103">There are a variety of ways to add data from your data source to a **Recordset**. The technique you use depends on the needs of your application and the capabilities of your provider.</span></span>

