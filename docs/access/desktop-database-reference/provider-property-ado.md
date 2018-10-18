---
<span data-ttu-id="28d04-101"><<<<<<< Título HEAD: proveedor (propiedad) (ADO) TOCTitle: proveedor (propiedad) (ADO) === título: proveedor (propiedad, ADO) TOCTitle: proveedor (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="28d04-101"><<<<<<< HEAD title: Provider Property (ADO) TOCTitle: Provider Property (ADO) ======= title: Provider property (ADO) TOCTitle: Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="28d04-102">Master ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: ms.date 48543543: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="28d04-102">master ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15) ms:contentKeyID: 48543543 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="28d04-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="28d04-103"><<<<<<< HEAD</span></span>
# <a name="provider-property-ado"></a><span data-ttu-id="28d04-104">Provider (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="28d04-104">Provider Property (ADO)</span></span>
=======
# <a name="provider-property-ado"></a><span data-ttu-id="28d04-105">Proveedor (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="28d04-105">Provider property (ADO)</span></span>
>>>>>>> <span data-ttu-id="28d04-106">master</span><span class="sxs-lookup"><span data-stu-id="28d04-106">master</span></span>


<span data-ttu-id="28d04-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="28d04-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="28d04-108">Indica el nombre del proveedor para un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="28d04-108">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="28d04-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="28d04-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="28d04-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="28d04-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="28d04-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="28d04-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="28d04-112">master</span><span class="sxs-lookup"><span data-stu-id="28d04-112">master</span></span>

<span data-ttu-id="28d04-113">Establece o devuelve un valor de tipo **String** que indica el nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="28d04-113">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="28d04-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28d04-114">Remarks</span></span>

<span data-ttu-id="28d04-p101">Utilice la propiedad **Provider** para establecer o devolver el nombre del proveedor de una conexión. Esta propiedad también puede establecerse mediante el contenido de la propiedad [ConnectionString](connectionstring-property-ado.md) o el argumento *ConnectionString* del método [Open](open-method-ado-connection.md); sin embargo, la especificación de un proveedor en más de un lugar mientras se llama al método **Open** pueda dar lugar a resultados impredecibles. Si no se especifica ningún proveedor, el valor predeterminado de la propiedad será MSDASQL ([Proveedor de Microsoft OLE DB para ODBC](microsoft-ole-db-provider-for-odbc.md)).</span><span class="sxs-lookup"><span data-stu-id="28d04-p101">Use the **Provider** property to set or return the name of the provider for a connection. This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results. If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="28d04-p102">La propiedad **Provider** es de lectura y escritura cuando la conexión está cerrada y de sólo lectura cuando está abierta. El valor no tiene ningún efecto hasta que se abre el objeto **Connection** o se obtiene acceso a la colección [Properties](properties-collection-ado.md) del objeto **Connection**. Si el valor no es válido, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="28d04-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>

