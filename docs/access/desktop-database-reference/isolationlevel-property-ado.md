---
<span data-ttu-id="48815-101"><<<<<<< Título HEAD: IsolationLevel (propiedad) (ADO) TOCTitle: IsolationLevel (propiedad) (ADO) === título: IsolationLevel (propiedad, ADO) TOCTitle: IsolationLevel (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="48815-101"><<<<<<< HEAD title: IsolationLevel Property (ADO) TOCTitle: IsolationLevel Property (ADO) ======= title: IsolationLevel property (ADO) TOCTitle: IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="48815-102">Master ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: ms.date 48543493: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="48815-102">master ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) ms:contentKeyID: 48543493 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="48815-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="48815-103"><<<<<<< HEAD</span></span>
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="48815-104">IsolationLevel (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="48815-104">IsolationLevel Property (ADO)</span></span>
=======
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="48815-105">IsolationLevel (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="48815-105">IsolationLevel property (ADO)</span></span>
>>>>>>> <span data-ttu-id="48815-106">master</span><span class="sxs-lookup"><span data-stu-id="48815-106">master</span></span>


<span data-ttu-id="48815-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="48815-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="48815-108">Indica el nivel de aislamiento de un objeto [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="48815-108">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="48815-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="48815-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="48815-110">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="48815-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="48815-111">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="48815-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="48815-112">master</span><span class="sxs-lookup"><span data-stu-id="48815-112">master</span></span>

<span data-ttu-id="48815-p101">Establece o devuelve un valor de tipo [IsolationLevelEnum](isolationlevelenum.md). El valor predeterminado es **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="48815-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="48815-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48815-115">Remarks</span></span>

<span data-ttu-id="48815-p102">Use la propiedad **IsolationLevel** para establecer el nivel de aislamiento de un objeto **Connection**. El valor no se aplica hasta la siguiente vez que se llama al método [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si el nivel de aislamiento solicitado no está disponible, el proveedor puede devolver el siguiente mayor valor de aislamiento.</span><span class="sxs-lookup"><span data-stu-id="48815-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="48815-119">La propiedad **IsolationLevel** es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="48815-119">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="48815-120">**Uso de servicio de datos remotos** Cuando se usa en un objeto Connection de cliente, se puede establecer la propiedad **IsolationLevel** sólo en **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="48815-120">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="48815-p103">Puesto que los usuarios están trabajando con objetos **Recordset** desconectados en una memoria caché del cliente, puede haber problemas de multiusuario. Por ejemplo, cuando dos usuarios diferentes intenten actualizar el mismo registro, el Servicio de datos remoto sólo permitirá que "gane" el usuario que actualice el registro en primer lugar. La solicitud de actualización del segundo usuario dará lugar a un error.</span><span class="sxs-lookup"><span data-stu-id="48815-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

