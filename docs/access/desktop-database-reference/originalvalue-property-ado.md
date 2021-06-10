---
title: Propiedad OriginalValue (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288185"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="90fa6-102">Propiedad OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="90fa6-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="90fa6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="90fa6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90fa6-104">Indica el valor de un objeto [Field](field-object-ado.md) que existía en el registro antes de la realización de cualquier cambio.</span><span class="sxs-lookup"><span data-stu-id="90fa6-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="90fa6-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90fa6-105">Return value</span></span>

<span data-ttu-id="90fa6-106">Devuelve un valor de tipo **Variant** que representa el valor de un campo antes de la realización de cualquier cambio.</span><span class="sxs-lookup"><span data-stu-id="90fa6-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="90fa6-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90fa6-107">Remarks</span></span>

<span data-ttu-id="90fa6-108">Utilice la propiedad **OriginalValue** para devolver el valor original de campo de un campo del registro actual.</span><span class="sxs-lookup"><span data-stu-id="90fa6-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="90fa6-109">En *modo* de actualización inmediata (en el que el proveedor escribe cambios en el origen de datos subyacente después de llamar al método [Update),](update-method-ado.md) la propiedad **OriginalValue** devuelve el valor de campo que existía antes de los cambios (es decir, desde la última llamada al método **Update).**</span><span class="sxs-lookup"><span data-stu-id="90fa6-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="90fa6-110">Es el mismo valor que usa el método [CancelUpdate](cancelupdate-method-ado.md) para sustituir a la propiedad [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="90fa6-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="90fa6-p102">En el *modo de actualización por lotes* (en el que el proveedor almacena varios cambios en caché y los escribe en el origen de datos subyacente sólo cuando se llama al método [UpdateBatch](updatebatch-method-ado.md)), la propiedad **OriginalValue** devuelve el valor de campo que existía antes de la realización de cualquier cambio (es decir, desde la última llamada al método **UpdateBatch**). Es el mismo valor que utiliza el método [CancelBatch](cancelbatch-method-ado.md) para sustituir a la propiedad **Value**. Cuando se utiliza esta propiedad con la propiedad [UnderlyingValue](underlyingvalue-property-ado.md), es posible solucionar conflictos que surgen a partir de las actualizaciones por lotes.</span><span class="sxs-lookup"><span data-stu-id="90fa6-p102">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call). This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property. When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="90fa6-114">Record</span><span class="sxs-lookup"><span data-stu-id="90fa6-114">Record</span></span>

<span data-ttu-id="90fa6-115">En los objetos [Record](record-object-ado.md), la propiedad **OriginalValue** estará vacía para los campos agregados antes de la llamada al método [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="90fa6-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

