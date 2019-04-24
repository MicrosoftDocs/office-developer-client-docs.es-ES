---
title: Usar CacheSize (referencia de base de datos de escritorio de Access)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 94e84ad8c8a87a6537c1abefe12427ecad0c0187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312127"
---
# <a name="using-cachesize"></a><span data-ttu-id="69a39-102">Uso de CacheSize</span><span class="sxs-lookup"><span data-stu-id="69a39-102">Using CacheSize</span></span>

<span data-ttu-id="69a39-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="69a39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="69a39-p101">Use la propiedad **CacheSize** para controlar el número de registros que se van a recuperar a la vez en la memoria local del proveedor. Por ejemplo, si el valor de **CacheSize** es 10, tras abrir el objeto **Recordset**, el proveedor recupera los 10 primeros registros en la memoria local. Cuando el usuario se mueve por el objeto **Recordset**, el proveedor devuelve los datos desde el búfer de memoria local. Cuando el usuario se desplaza hasta un punto situado más allá del último registro de la memoria caché, el proveedor recupera en la memoria caché los 10 siguientes registros del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="69a39-p101">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="69a39-p102">[!NOTA] **CacheSize** se basa en la propiedad específica del proveedor **Número máximo de filas abiertas** (en la colección **Properties** del objeto **Recordset** ). No puede establecer **CacheSize** en un valor mayor que el valor de **Número máximo de filas abiertas**. Para modificar el número de filas que puede abrir el proveedor, establezca el valor de **Número máximo de filas abiertas**.</span><span class="sxs-lookup"><span data-stu-id="69a39-p102">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object). You cannot set **CacheSize** to a value greater than **Maximum Open Rows**. To modify the number of rows that can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="69a39-p103">El valor de **CacheSize** se puede ajustar durante la vida del objeto **Recordset**, pero cambiar este valor solo afecta al número de registros en la memoria caché después de recuperaciones posteriores desde el origen de datos. Si solo se cambia el valor de la propiedad, el contenido de la memoria caché en ese momento no cambiará.</span><span class="sxs-lookup"><span data-stu-id="69a39-p103">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="69a39-113">Si el número de registros que se van a recuperar es menor que el valor de **CacheSize**, el proveedor devuelve los registros restantes y no se genera ningún error.</span><span class="sxs-lookup"><span data-stu-id="69a39-113">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="69a39-114">No se puede establecer **CacheSize** en cero, ya que devolvería un error.</span><span class="sxs-lookup"><span data-stu-id="69a39-114">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="69a39-p104">Los registros recuperados de la caché no reflejan cambios simultáneos realizados por otros usuarios en los datos del origen. Para forzar una actualización de todos los datos en caché, utilice el método [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="69a39-p104">Records retrieved from the cache do not reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="69a39-p105">Si **CacheSize** se establece en un valor mayor que 1, los métodos de navegación ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext y MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) pueden provocar la navegación a un registro eliminado, si la eliminación se efectuó después de haber recuperado los registros. Después de la recuperación inicial, las eliminaciones posteriores no se reflejarán en su caché de datos hasta que intente obtener acceso a un valor de datos de una fila eliminada. Sin embargo, si se establece **CacheSize** en 1, se elimina este problema porque no se pueden recuperar filas eliminadas.</span><span class="sxs-lookup"><span data-stu-id="69a39-p105">If **CacheSize** is set to a value greater than 1, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.</span></span>

