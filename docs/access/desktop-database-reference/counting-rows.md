---
title: El recuento de filas (referencia de escritorio de la base de datos de Access)
TOCTitle: Counting Rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93a583ef0a8f0ef287835eebdd9d68cf726a19df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485707"
---
# <a name="counting-rows"></a><span data-ttu-id="b996f-102">Contar filas</span><span class="sxs-lookup"><span data-stu-id="b996f-102">Counting Rows</span></span>


<span data-ttu-id="b996f-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b996f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b996f-p101">La propiedad **RecordCount** devuelve un valor **Long** que indica el número de registros del **Recordset**. Use la propiedad **RecordCount** para determinar cuántos registros hay en un objeto **Recordset**. La propiedad devuelve -1 cuando ADO no puede determinar el número de registros o si el proveedor o tipo de cursor no admite **RecordCount**. La lectura de la propiedad **RecordCount** de un **Recordset** cerrado causa un error.</span><span class="sxs-lookup"><span data-stu-id="b996f-p101">The **RecordCount** property returns a **Long** value that indicates the number of records in the **Recordset**. Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="b996f-p102">La propiedad **RecordCount** depende de las capacidades del proveedor y del tipo de cursor. La propiedad **RecordCount** devolverá -1 para un cursor de sólo avance, el recuento real para un cursor estático o de conjunto de claves, y -1 o el recuento real para un cursor dinámico, en función del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="b996f-p102">The **RecordCount** property depends on the capabilities of the provider and the type of cursor. The **RecordCount** property will return -1 for a forward-only cursor, the actual count for a static or keyset cursor, and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

<span data-ttu-id="b996f-110">El ejemplo de **conjunto de registros** presentado en [Examinar datos](chapter-3-examining-data.md) devolverá – 1 porque se abrió un cursor de sólo avance.</span><span class="sxs-lookup"><span data-stu-id="b996f-110">The sample **Recordset** introduced in [Examining Data](chapter-3-examining-data.md) would return –1 because a forward-only cursor was opened.</span></span> <span data-ttu-id="b996f-111">Para usar la propiedad **RecordCount**, debería abrir el **Recordset** con un cursor más complejo (estático o conjunto de claves).</span><span class="sxs-lookup"><span data-stu-id="b996f-111">In order to use the **RecordCount** property, you would need to open the **Recordset** with a more sophisticated cursor (static or keyset).</span></span>

<span data-ttu-id="b996f-p104">En algunos casos, puede que el proveedor o el cursor no puedan proporcionar el valor de **RecordCount** sin obtener primero todos los registros desde el origen de datos. Para forzar este tipo de búsqueda, llame al método **MoveLast** de **Recordset** antes de llamar a **RecordCount**</span><span class="sxs-lookup"><span data-stu-id="b996f-p104">In certain cases, your provider or cursor might be unable to provide the **RecordCount** value without first fetching all records from the data source. To force this type of fetch, call the **Recordset** **MoveLast** method before calling **RecordCount**.</span></span>

<span data-ttu-id="b996f-114">Si reemplazara la línea de código que llama al método **Open** de **Recordset** por lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b996f-114">If you were to replace the line of code that calls the **Recordset** **Open** method with the following:</span></span>

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="b996f-p105">podría utilizar la propiedad **RecordCount**, ya que los cursores estáticos del [Proveedor de Microsoft OLE DB para SQL Server](microsoft-ole-db-provider-for-sql-server.md) admiten **RecordCount**. Por ejemplo, el código siguiente imprimirá el número de registros devueltos por el comando a la ventana de depuración, suponiendo que el cursor admita la propiedad **RecordCount**:</span><span class="sxs-lookup"><span data-stu-id="b996f-p105">you would be able to use the **RecordCount** property because static cursors with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) support **RecordCount**. For example, the following code would print out the number of records returned by the command to the debug window, assuming the cursor supports the **RecordCount** property:</span></span>

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

<span data-ttu-id="b996f-117">A partir de este momento, se supone que se utilizan estas opciones más eficaces (pero más costosas) de tipo de cursor y bloqueo.</span><span class="sxs-lookup"><span data-stu-id="b996f-117">From this point forward, assume that these more capable (but more expensive) cursor and lock type settings are used.</span></span>
