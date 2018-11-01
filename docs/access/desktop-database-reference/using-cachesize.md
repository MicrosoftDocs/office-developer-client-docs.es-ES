---
title: Utilizar CacheSize (referencia de escritorio de la base de datos de Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa624c545d17ef0d56a076b3d30326bacd2c6edf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871965"
---
# <a name="using-cachesize"></a><span data-ttu-id="cc62a-102">Uso de CacheSize</span><span class="sxs-lookup"><span data-stu-id="cc62a-102">Using CacheSize</span></span>


<span data-ttu-id="cc62a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc62a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc62a-p101">Use la propiedad **CacheSize** para controlar el número de registros que se van a recuperar a la vez en la memoria local del proveedor. Por ejemplo, si el valor de **CacheSize** es 10, tras abrir el objeto **Recordset**, el proveedor recupera los 10 primeros registros en la memoria local. Cuando el usuario se mueve por el objeto **Recordset**, el proveedor devuelve los datos desde el búfer de memoria local. Cuando el usuario se desplaza hasta un punto situado más allá del último registro de la memoria caché, el proveedor recupera en la memoria caché los 10 siguientes registros del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="cc62a-p101">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="cc62a-p102">[!NOTA] <STRONG>CacheSize</STRONG> se basa en la propiedad específica del proveedor <STRONG>Número máximo de filas abiertas</STRONG> (en la colección <STRONG>Properties</STRONG> del objeto <STRONG>Recordset</STRONG> ). No puede establecer <STRONG>CacheSize</STRONG> en un valor mayor que el valor de <STRONG>Número máximo de filas abiertas</STRONG>. Para modificar el número de filas que puede abrir el proveedor, establezca el valor de <STRONG>Número máximo de filas abiertas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="cc62a-p102"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object). You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>. To modify the number of rows that can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="cc62a-p103">El valor de **CacheSize** se puede ajustar durante la vida del objeto **Recordset**, pero cambiar este valor solo afecta al número de registros en la memoria caché después de recuperaciones posteriores desde el origen de datos. Si solo se cambia el valor de la propiedad, el contenido de la memoria caché en ese momento no cambiará.</span><span class="sxs-lookup"><span data-stu-id="cc62a-p103">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="cc62a-113">Si hay menos registros para recuperar que la cantidad especificada con **CacheSize**, el proveedor devuelve los registros restantes y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="cc62a-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="cc62a-114">No se puede establecer **CacheSize** en cero, ya que devolvería un error.</span><span class="sxs-lookup"><span data-stu-id="cc62a-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="cc62a-p104">Los registros recuperados de la caché no reflejan cambios simultáneos realizados por otros usuarios en los datos del origen. Para forzar una actualización de todos los datos en caché, utilice el método [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cc62a-p104">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="cc62a-p105">Si **CacheSize** se establece en un valor mayor que 1, los métodos de navegación ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext y MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) pueden provocar la navegación a un registro eliminado, si la eliminación se efectuó después de haber recuperado los registros. Después de la recuperación inicial, las eliminaciones posteriores no se reflejarán en su caché de datos hasta que intente obtener acceso a un valor de datos de una fila eliminada. Sin embargo, si se establece **CacheSize** en 1, se elimina este problema porque no se pueden recuperar filas eliminadas.</span><span class="sxs-lookup"><span data-stu-id="cc62a-p105">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

