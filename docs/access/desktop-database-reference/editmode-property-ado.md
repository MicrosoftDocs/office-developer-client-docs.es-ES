---
title: EditMode (propiedad, ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293612"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="53851-102">EditMode (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="53851-102">EditMode property (ADO)</span></span>


<span data-ttu-id="53851-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53851-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53851-104">Indica el estado de modificación del registro actual.</span><span class="sxs-lookup"><span data-stu-id="53851-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="53851-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53851-105">Return value</span></span>

<span data-ttu-id="53851-106">Devuelve un valor [EditModeEnum](editmodeenum.md).</span><span class="sxs-lookup"><span data-stu-id="53851-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53851-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="53851-107">Remarks</span></span>

<span data-ttu-id="53851-p101">ADO mantiene un búfer de modificación asociado al registro actual. Esta propiedad indica si se han realizado cambios en este búfer o si se ha creado un registro nuevo. Utilice la propiedad **EditMode** para determinar el estado de modificación del registro actual. Puede probar cambios pendientes si un proceso de modificación se ha interrumpido y determinar si debe utilizar el método [Update](update-method-ado.md) o [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="53851-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="53851-112">Vea el método [AddNew](addnew-method-ado.md) para obtener una descripción más detallada de la propiedad **EditMode** en condiciones de modificación diferentes.</span><span class="sxs-lookup"><span data-stu-id="53851-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="53851-113">Cuando una llamada a [Delete](delete-method-ado-recordset.md) no elimina correctamente el registro o los registros en el origen de datos (debido a infracciones de integridad referencial, por ejemplo), el [objeto Recordset](recordset-object-ado.md) permanecerá en modo de edición (**EditMode** = \*\*adEditInProgress \*\*).</span><span class="sxs-lookup"><span data-stu-id="53851-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="53851-114">Eso significa que es necesario llamar a **CancelUpdate** antes de quitar el registro actual (con [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) o [Close](close-method-ado.md), por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="53851-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <span data-ttu-id="53851-p103">[!NOTA] **EditMode** puede devolver un valor válido únicamente si hay un registro actual. **EditMode** devolverá un error si [BOF o EOF](bof-eof-properties-ado.md) son True o si se ha eliminado el registro actual.</span><span class="sxs-lookup"><span data-stu-id="53851-p103">**EditMode** can return a valid value only if there is a current record. **EditMode** will return an error if [BOF or EOF](bof-eof-properties-ado.md) is true, or if the current record has been deleted.</span></span>


