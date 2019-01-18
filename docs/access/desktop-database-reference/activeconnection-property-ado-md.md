---
title: ActiveConnection (propiedad, ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 372dac11500647af75881ae6b4aee22a391a32c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703191"
---
# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="004d3-102">ActiveConnection (propiedad, ADO MD)</span><span class="sxs-lookup"><span data-stu-id="004d3-102">ActiveConnection property (ADO MD)</span></span>

<span data-ttu-id="004d3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="004d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="004d3-104">Indica a qué objeto [Connection](connection-object-ado.md) de ADO pertenece el conjunto de celdas o el catálogo activo.</span><span class="sxs-lookup"><span data-stu-id="004d3-104">Indicates to which ADO [Connection](connection-object-ado.md) object the current cellset or catalog currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="004d3-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="004d3-105">Settings and return values</span></span>

<span data-ttu-id="004d3-p101">Establece o devuelve un valor de tipo **Variant** que contiene una cadena que define una conexión o un objeto **Connection**. El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="004d3-p101">Sets or returns a **Variant** that contains a string defining a connection or **Connection** object. The default is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="004d3-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="004d3-108">Remarks</span></span>

<span data-ttu-id="004d3-p102">Esta propiedad se puede establecer en un objeto **Connection** de ADO válido o en una cadena de conexión válida. Cuando esta propiedad se establece en una cadena de conexión, el proveedor crea un nuevo objeto **Connection** que utiliza esta definición y abre la conexión.</span><span class="sxs-lookup"><span data-stu-id="004d3-p102">You can set this property to a valid ADO **Connection** object or to a valid connection string. When this property is set to a connection string, the provider creates a new **Connection** object using this definition and opens the connection.</span></span>

<span data-ttu-id="004d3-111">Si usa el argumento **ActiveConnection** del método [Open](open-method-ado-md.md) para abrir un objeto [Cellset](cellset-object-ado-md.md), la propiedad **ActiveConnection** heredará el valor del argumento.</span><span class="sxs-lookup"><span data-stu-id="004d3-111">If you use the **ActiveConnection** argument of the [Open](open-method-ado-md.md) method to open a [Cellset](cellset-object-ado-md.md) object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="004d3-p103">Si se establece la propiedad **ActiveConnection** de un objeto [Catalog](catalog-object-ado-md.md) en **Nothing**, se liberarán los datos asociados, incluidos los datos de la colección [CubeDefs](cubedefs-collection-ado-md.md) y cualquier objeto [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) y [Member](member-object-ado-md.md) asociado. Cerrar un objeto **Connection** que se haya utilizado para abrir un **catálogo** tiene el mismo efecto que establecer la propiedad **ActiveConnection** en **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="004d3-p103">Setting the **ActiveConnection** property of a [Catalog](catalog-object-ado-md.md) object to **Nothing** releases the associated data, including data in the [CubeDefs](cubedefs-collection-ado-md.md) collection and any related [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md) objects. Closing a **Connection** object that was used to open a **Catalog** has the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

<span data-ttu-id="004d3-114">Si se cambia la base de datos predeterminada de la conexión a la que se hace referencia con la propiedad **ActiveConnection** de un objeto **Catalog**, el contenido del **catálogo** pierde su validez.</span><span class="sxs-lookup"><span data-stu-id="004d3-114">Changing the default database of the connection referenced by the **ActiveConnection** property of a **Catalog** object invalidates the contents of the **Catalog**.</span></span>

<span data-ttu-id="004d3-115">Si intenta cambiar la propiedad **ActiveConnection** para un objeto **Cellset** abierto, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="004d3-115">An error will occur if you attempt to change the **ActiveConnection** property for an open **Cellset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="004d3-p104">[!NOTA] En Visual Basic, recuerde utilizar la palabra clave **Set** al establecer la propiedad **ActiveConnection** en un objeto **Connection**. Si omite la palabra clave **Set**, en realidad estará estableciendo la propiedad **ActiveConnection** igual que la propiedad predeterminada del objeto **Connection**, **ConnectionString**. El código funcionará, pero se creará una conexión adicional al origen de datos, lo que puede afectar negativamente al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="004d3-p104">In Visual Basic, remember to use the **Set** keyword when setting the **ActiveConnection** property to a **Connection** object. If you omit the **Set** keyword, you will actually be setting the **ActiveConnection** property equal to the **Connection** object's default property, **ConnectionString**. The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span>

<span data-ttu-id="004d3-p105">Si usa el proveedor de datos MSOLAP, establezca el origen de datos de una cadena de conexión en un nombre de servidor y establezca el catálogo inicial en el nombre de un catálogo del origen de datos. Para conectarse a un archivo de cubo que esté desconectado de un servidor, establezca la ubicación en la ruta completa de acceso al archivo .CUB. En cualquier caso, establezca el proveedor en el nombre de proveedor. Por ejemplo, la cadena siguiente establece una conexión a un catálogo que se denomina Bobs Video Store en un servidor denominado Servername con el proveedor MSOLAP:</span><span class="sxs-lookup"><span data-stu-id="004d3-p105">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source. To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file. In either case, set the provider to the provider name. For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:</span></span>

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

<span data-ttu-id="004d3-123">La siguiente cadena se conecta a un archivo de cubo local en la ubicación C:\\MSDASDK\\ejemplos\\oledb\\olap\\datos\\bobsvid.cub:</span><span class="sxs-lookup"><span data-stu-id="004d3-123">The following string connects to a local cube file at the location C:\\MSDASDK\\samples\\oledb\\olap\\data\\bobsvid.cub:</span></span>

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

