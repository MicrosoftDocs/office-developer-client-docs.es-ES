---
title: UnderlyingValue (propiedad, ADO)
TOCTitle: UnderlyingValue Property (ADO)
ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15)
ms:contentKeyID: 48548782
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10140d0cc4105ed46ddaaf48e4c827f364adc90c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485477"
---
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="9991e-102">UnderlyingValue (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="9991e-102">UnderlyingValue Property (ADO)</span></span>


<span data-ttu-id="9991e-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9991e-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="9991e-104">Indica el valor actual de un objeto [Field](field-object-ado.md) de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9991e-104">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

## <a name="return-value"></a><span data-ttu-id="9991e-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9991e-105">Return Value</span></span>

<span data-ttu-id="9991e-106">Devuelve un valor de tipo **Variant** que indica el valor del objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="9991e-106">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9991e-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9991e-107">Remarks</span></span>

<span data-ttu-id="9991e-p101">Use la propiedad **UnderlyingValue** para devolver el valor actual del campo de la base de datos. El valor del campo de la propiedad **UnderlyingValue** es el valor visible en la transacción y puede ser el resultado de una actualización reciente por parte de otra transacción. Puede diferir de la propiedad [OriginalValue](originalvalue-property-ado.md), que refleja el valor devuelto originalmente al objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9991e-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="9991e-p102">Es similar a utilizar el método [Resync](resync-method-ado.md), aunque la propiedad **UnderlyingValue** sólo devuelve el valor de un campo específico del registro actual. Se trata del mismo valor que el método [Resync](resync-method-ado.md) utiliza para sustituir a la propiedad [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9991e-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="9991e-113">Cuando esta propiedad se utiliza con la propiedad **OriginalValue**, es posible solucionar conflictos que surgen a partir de las actualizaciones por lotes.</span><span class="sxs-lookup"><span data-stu-id="9991e-113">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="9991e-114">Record</span><span class="sxs-lookup"><span data-stu-id="9991e-114">Record</span></span>

<span data-ttu-id="9991e-115">En los objetos [Record](record-object-ado.md), esta propiedad estará vacía para los campos agregados antes de la llamada al método [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9991e-115">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

