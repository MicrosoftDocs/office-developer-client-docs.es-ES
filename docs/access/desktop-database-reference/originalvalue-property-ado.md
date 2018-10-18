---
<span data-ttu-id="07604-101"><<<<<<< Título HEAD: OriginalValue (propiedad) (ADO) TOCTitle: OriginalValue (propiedad) (ADO) === título: OriginalValue (propiedad, ADO) TOCTitle: OriginalValue (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="07604-101"><<<<<<< HEAD title: OriginalValue Property (ADO) TOCTitle: OriginalValue Property (ADO) ======= title: OriginalValue property (ADO) TOCTitle: OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="07604-102">Master ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: ms.date 48542974: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="07604-102">master ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="07604-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="07604-103"><<<<<<< HEAD</span></span>
# <a name="originalvalue-property-ado"></a><span data-ttu-id="07604-104">OriginalValue (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="07604-104">OriginalValue Property (ADO)</span></span>
=======
# <a name="originalvalue-property-ado"></a><span data-ttu-id="07604-105">OriginalValue (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="07604-105">OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="07604-106">master</span><span class="sxs-lookup"><span data-stu-id="07604-106">master</span></span>

<span data-ttu-id="07604-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07604-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07604-108">Indica el valor de un objeto [Field](field-object-ado.md) que existía en el registro antes de la realización de cualquier cambio.</span><span class="sxs-lookup"><span data-stu-id="07604-108">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

<span data-ttu-id="07604-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="07604-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="07604-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07604-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="07604-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07604-111">Return value</span></span>
>>>>>>> <span data-ttu-id="07604-112">master</span><span class="sxs-lookup"><span data-stu-id="07604-112">master</span></span>

<span data-ttu-id="07604-113">Devuelve un valor de tipo **Variant** que representa el valor de un campo antes de la realización de cualquier cambio.</span><span class="sxs-lookup"><span data-stu-id="07604-113">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="07604-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07604-114">Remarks</span></span>

<span data-ttu-id="07604-115">Utilice la propiedad **OriginalValue** para devolver el valor original de campo de un campo del registro actual.</span><span class="sxs-lookup"><span data-stu-id="07604-115">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="07604-116">En el *modo de actualización inmediata* (en la que el proveedor escribe los cambios en el origen de datos subyacente después de llamar al método [Update](update-method-ado.md) ), la propiedad **OriginalValue** devuelve el valor de campo que existía antes de cualquier cambio (es decir, desde el última llamada al método **Update** ).</span><span class="sxs-lookup"><span data-stu-id="07604-116">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="07604-117">Es el mismo valor que usa el método [CancelUpdate](cancelupdate-method-ado.md) para sustituir a la propiedad [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="07604-117">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="07604-118">En *el modo de actualización por lotes* (en el que el proveedor almacena varios cambios en caché y los escribe en el origen de datos subyacente sólo cuando se llama al método [UpdateBatch](updatebatch-method-ado.md) ), la propiedad **OriginalValue** devuelve el valor de campo que existía antes de cualquier los cambios (es decir, desde el último método **UpdateBatch** (llamada).</span><span class="sxs-lookup"><span data-stu-id="07604-118">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="07604-119">Es el mismo valor que utiliza el método [CancelBatch](cancelbatch-method-ado.md) para sustituir a la propiedad **Value**.</span><span class="sxs-lookup"><span data-stu-id="07604-119">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="07604-120">Cuando se utiliza esta propiedad con la propiedad [UnderlyingValue](underlyingvalue-property-ado.md), es posible solucionar conflictos que surgen a partir de las actualizaciones por lotes.</span><span class="sxs-lookup"><span data-stu-id="07604-120">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="07604-121">Record</span><span class="sxs-lookup"><span data-stu-id="07604-121">Record</span></span>

<span data-ttu-id="07604-122">En los objetos [Record](record-object-ado.md), la propiedad **OriginalValue** estará vacía para los campos agregados antes de la llamada al método [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="07604-122">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

