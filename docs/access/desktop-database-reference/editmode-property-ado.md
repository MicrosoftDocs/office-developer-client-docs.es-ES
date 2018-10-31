---
<span data-ttu-id="aef6f-101"><<<<<<< Título HEAD: EditMode (propiedad) (ADO) TOCTitle: EditMode (propiedad) (ADO) === título: EditMode (propiedad, ADO) TOCTitle: EditMode (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="aef6f-101"><<<<<<< HEAD title: EditMode Property (ADO) TOCTitle: EditMode Property (ADO) ======= title: EditMode property (ADO) TOCTitle: EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aef6f-102">Master ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: ms.date 48543867: 18/09/2015 mtps_version: Office.15</span><span class="sxs-lookup"><span data-stu-id="aef6f-102">master ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID: 48543867 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="aef6f-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="aef6f-103"><<<<<<< HEAD</span></span>
# <a name="editmode-property-ado"></a><span data-ttu-id="aef6f-104">EditMode (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="aef6f-104">EditMode Property (ADO)</span></span>
=======
# <a name="editmode-property-ado"></a><span data-ttu-id="aef6f-105">EditMode (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="aef6f-105">EditMode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aef6f-106">master</span><span class="sxs-lookup"><span data-stu-id="aef6f-106">master</span></span>


<span data-ttu-id="aef6f-107">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aef6f-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aef6f-108">Indica el estado de modificación del registro actual.</span><span class="sxs-lookup"><span data-stu-id="aef6f-108">Indicates the editing status of the current record.</span></span>

<span data-ttu-id="aef6f-109"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="aef6f-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="aef6f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aef6f-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="aef6f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aef6f-111">Return value</span></span>
>>>>>>> <span data-ttu-id="aef6f-112">master</span><span class="sxs-lookup"><span data-stu-id="aef6f-112">master</span></span>

<span data-ttu-id="aef6f-113">Devuelve un valor [EditModeEnum](editmodeenum.md).</span><span class="sxs-lookup"><span data-stu-id="aef6f-113">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aef6f-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="aef6f-114">Remarks</span></span>

<span data-ttu-id="aef6f-p101">ADO mantiene un búfer de modificación asociado al registro actual. Esta propiedad indica si se han realizado cambios en este búfer o si se ha creado un registro nuevo. Utilice la propiedad **EditMode** para determinar el estado de modificación del registro actual. Puede probar cambios pendientes si un proceso de modificación se ha interrumpido y determinar si debe utilizar el método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="aef6f-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="aef6f-119">Vea el método [AddNew](addnew-method-ado.md) para obtener una descripción más detallada de la propiedad **EditMode** en condiciones de modificación diferentes.</span><span class="sxs-lookup"><span data-stu-id="aef6f-119">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="aef6f-120">Cuando una llamada a [Eliminar](delete-method-ado-recordset.md) no elimina correctamente el registro o registros en los datos de origen (debido a, por ejemplo, infracciones de integridad referencial), el [objeto Recordset](recordset-object-ado.md) permanecerá en modo de edición (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="aef6f-120">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="aef6f-121">Eso significa que es necesario llamar a **CancelUpdate** antes de quitar el registro actual (con [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) o [Close](close-method-ado.md), por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="aef6f-121">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="aef6f-p103">[!NOTA] **EditMode** puede devolver un valor válido únicamente si hay un registro actual. **EditMode** devolverá un error si [BOF o EOF](bof-eof-properties-ado.md) son True o si se ha eliminado el registro actual.</span><span class="sxs-lookup"><span data-stu-id="aef6f-p103">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


