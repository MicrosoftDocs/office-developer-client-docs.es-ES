---
title: EditMode (propiedad, ADO)
TOCTitle: EditMode Property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6c8377e0fa0fc2db1ec2d376ee3c8b9f16e8c99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484037"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="c5dbc-102">EditMode (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="c5dbc-102">EditMode Property (ADO)</span></span>


<span data-ttu-id="c5dbc-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c5dbc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c5dbc-104">Indica el estado de modificación del registro actual.</span><span class="sxs-lookup"><span data-stu-id="c5dbc-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5dbc-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5dbc-105">Return Value</span></span>

<span data-ttu-id="c5dbc-106">Devuelve un valor [EditModeEnum](editmodeenum.md).</span><span class="sxs-lookup"><span data-stu-id="c5dbc-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5dbc-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c5dbc-107">Remarks</span></span>

<span data-ttu-id="c5dbc-p101">ADO mantiene un búfer de modificación asociado al registro actual. Esta propiedad indica si se han realizado cambios en este búfer o si se ha creado un registro nuevo. Utilice la propiedad **EditMode** para determinar el estado de modificación del registro actual. Puede probar cambios pendientes si un proceso de modificación se ha interrumpido y determinar si debe utilizar el método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c5dbc-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="c5dbc-112">Vea el método [AddNew](addnew-method-ado.md) para obtener una descripción más detallada de la propiedad **EditMode** en condiciones de modificación diferentes.</span><span class="sxs-lookup"><span data-stu-id="c5dbc-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="c5dbc-113">Cuando una llamada a [Eliminar](delete-method-ado-recordset.md) no elimina correctamente el registro o registros en los datos de origen (debido a, por ejemplo, infracciones de integridad referencial), el [objeto Recordset](recordset-object-ado.md) permanecerá en modo de edición (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="c5dbc-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="c5dbc-114">Eso significa que es necesario llamar a **CancelUpdate** antes de quitar el registro actual (con [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) o [Close](close-method-ado.md), por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="c5dbc-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <P><span data-ttu-id="c5dbc-p103">[!NOTA] <STRONG>EditMode</STRONG> puede devolver un valor válido únicamente si hay un registro actual. <STRONG>EditMode</STRONG> devolverá un error si <A href="bof-eof-properties-ado.md">BOF o EOF</A> son True o si se ha eliminado el registro actual.</span><span class="sxs-lookup"><span data-stu-id="c5dbc-p103"><STRONG>EditMode</STRONG> can return a valid value only if there is a current record. <STRONG>EditMode</STRONG> will return an error if <A href="bof-eof-properties-ado.md">BOF or EOF</A> is true, or if the current record has been deleted.</span></span></P>


