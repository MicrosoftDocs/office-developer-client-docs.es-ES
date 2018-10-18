---
<span data-ttu-id="de70f-101"><<<<<<< Título HEAD: DefaultDatabase (propiedad) (ADO) TOCTitle: DefaultDatabase (propiedad) (ADO) === título: DefaultDatabase (propiedad, ADO) TOCTitle: DefaultDatabase (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="de70f-101"><<<<<<< HEAD title: DefaultDatabase Property (ADO) TOCTitle: DefaultDatabase Property (ADO) ======= title: DefaultDatabase property (ADO) TOCTitle: DefaultDatabase property (ADO)</span></span>
>>>>>>> <span data-ttu-id="de70f-102">Master ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID: ms.date 48546784: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="de70f-102">master ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15) ms:contentKeyID: 48546784 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="de70f-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="de70f-103"><<<<<<< HEAD</span></span>
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="de70f-104">DefaultDatabase (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="de70f-104">DefaultDatabase Property (ADO)</span></span>
=======
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="de70f-105">DefaultDatabase (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="de70f-105">DefaultDatabase property (ADO)</span></span>
>>>>>>> <span data-ttu-id="de70f-106">master</span><span class="sxs-lookup"><span data-stu-id="de70f-106">master</span></span>


<span data-ttu-id="de70f-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de70f-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="de70f-108">Indica la base de datos predeterminada de un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="de70f-108">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="de70f-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="de70f-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="de70f-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="de70f-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="de70f-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="de70f-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="de70f-112">master</span><span class="sxs-lookup"><span data-stu-id="de70f-112">master</span></span>

<span data-ttu-id="de70f-113">Establece o devuelve un valor de tipo **String** que da como resultado el nombre de una base de datos que está disponible en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="de70f-113">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="de70f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="de70f-114">Remarks</span></span>

<span data-ttu-id="de70f-115">Utilice la propiedad **DefaultDatabase** para establecer o devolver el nombre de la base de datos predeterminada en un objeto **Connection** específico.</span><span class="sxs-lookup"><span data-stu-id="de70f-115">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="de70f-p101">Si hay una base de datos predeterminada, puede que las cadenas SQL utilicen una sintaxis incompleta para obtener acceso a los objetos de esa base de datos. Para obtener acceso a los objetos de una base de datos distinta de la especificada en la propiedad **DefaultDatabase**, los nombres de objeto deben incluir el nombre de la base de datos deseada. Tras establecer la conexión, el proveedor escribirá la información de la base de datos predeterminada en la propiedad **DefaultDatabase**. Algunos proveedores permiten sólo una base de datos por conexión, en cuyo caso no se puede cambiar el valor de la propiedad **DefaultDatabase**.</span><span class="sxs-lookup"><span data-stu-id="de70f-p101">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database. To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name. Upon connection, the provider will write default database information to the **DefaultDatabase** property. Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="de70f-120">Es posible que algunos orígenes de datos y proveedores no admitan esta característica y devuelvan un error o una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="de70f-120">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="de70f-121">**Uso de servicio de datos remotos** Esta propiedad no está disponible en un objeto de **conexión** de cliente.</span><span class="sxs-lookup"><span data-stu-id="de70f-121">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

