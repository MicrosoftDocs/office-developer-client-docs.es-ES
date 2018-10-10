---
title: CacheSize (propiedad, ADO)
TOCTitle: CacheSize Property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed4d104dcd6d0b90e6011a305cd3502cf671175b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485976"
---
# <a name="cachesize-property-ado"></a><span data-ttu-id="feccd-102">CacheSize (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="feccd-102">CacheSize Property (ADO)</span></span>


<span data-ttu-id="feccd-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="feccd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="feccd-104">Indica el número de registros de un objeto [Recordset](recordset-object-ado.md) que están almacenados en la memoria caché local.</span><span class="sxs-lookup"><span data-stu-id="feccd-104">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="feccd-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="feccd-105">Settings and Return Values</span></span>

<span data-ttu-id="feccd-p101">Establece o devuelve un valor de tipo **Long** que debe ser mayor que 0. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="feccd-p101">Sets or returns a **Long** value that must be greater than 0. Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="feccd-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="feccd-108">Remarks</span></span>

<span data-ttu-id="feccd-p102">Use la propiedad **CacheSize** para controlar el número de registros que se van a recuperar a la vez en la memoria local del proveedor. Por ejemplo, si el valor de **CacheSize** es 10, tras abrir el objeto **Recordset**, el proveedor recupera los 10 primeros registros en la memoria local. Cuando el usuario se mueve por el objeto **Recordset**, el proveedor devuelve los datos desde el búfer de memoria local. Cuando el usuario se desplaza hasta un punto situado más allá del último registro de la caché, el proveedor recupera en la memoria caché los 10 siguientes registros del origen de datos.</span><span class="sxs-lookup"><span data-stu-id="feccd-p102">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>


> [!NOTE]
> <P><span data-ttu-id="feccd-p103">[!NOTA] <STRONG>CacheSize</STRONG> se basa en la propiedad específica del proveedor <STRONG>Número máximo de filas abiertas</STRONG> (en la colección <STRONG>Properties</STRONG> del objeto <STRONG>Recordset</STRONG> ). No se puede establecer <STRONG>CacheSize</STRONG> en un valor mayor que el valor de <STRONG>Número máximo de filas abiertas</STRONG>. Para modificar el número de registros que el proveedor puede abrir, establezca el valor de <STRONG>Número máximo de filas abiertas</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="feccd-p103"><STRONG>CacheSize</STRONG> is based on the <STRONG>Maximum Open Rows</STRONG> provider-specific property (in the <STRONG>Properties</STRONG> collection of the <STRONG>Recordset</STRONG> object). You cannot set <STRONG>CacheSize</STRONG> to a value greater than <STRONG>Maximum Open Rows</STRONG>. To modify the number of rows which can be opened by the provider, set <STRONG>Maximum Open Rows</STRONG>.</span></span></P>



<span data-ttu-id="feccd-p104">El valor de **CacheSize** se puede ajustar a lo largo del ciclo de vida del objeto **Recordset**, pero al cambiar este valor, sólo se ve afectado el número de registros en la memoria caché después de recuperaciones subsiguientes desde el origen de datos. Al cambiar sólo el valor de esta propiedad, no se modificará el actual contenido de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="feccd-p104">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="feccd-118">Si hay menos registros para recuperar que la cantidad especificada con **CacheSize**, el proveedor devuelve los registros restantes y no se produce ningún error.</span><span class="sxs-lookup"><span data-stu-id="feccd-118">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="feccd-119">No se puede establecer **CacheSize** en cero, ya que devolvería un error.</span><span class="sxs-lookup"><span data-stu-id="feccd-119">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="feccd-p105">Los registros recuperados de la caché no reflejan los cambios concurrentes realizados por otros usuarios en el origen de datos. Para que se actualicen todos los datos almacenados en la caché, utilice el método [Resync](resync-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="feccd-p105">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="feccd-p106">Si el valor de **CacheSize** es mayor que 1, los métodos de navegación ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext y MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) pueden dar como resultado la navegación a un registro eliminado si la eliminación se ha producido después de recuperarse los registros. Después de la recuperación inicial, las eliminaciones posteriores no se reflejarán en la memoria caché de datos hasta que intente obtener acceso a un valor de datos de una fila eliminada. Sin embargo, si se establece el valor de **CacheSize** en 1, ya no existirá este problema ya que no se podrán recuperar las filas eliminadas.</span><span class="sxs-lookup"><span data-stu-id="feccd-p106">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

