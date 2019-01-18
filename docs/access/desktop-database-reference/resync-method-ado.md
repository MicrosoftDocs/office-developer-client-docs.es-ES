---
title: Resync (método, ADO)
TOCTitle: Resync method (ADO)
ms:assetid: f594a200-56e6-fcf5-9b0a-900c56377f24
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250251(v=office.15)
ms:contentKeyID: 48548717
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fa483d86dc345968607a0752f0552ddccfe7fef5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709876"
---
# <a name="resync-method-ado"></a><span data-ttu-id="5d0b5-102">Resync (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="5d0b5-102">Resync method (ADO)</span></span>

<span data-ttu-id="5d0b5-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d0b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d0b5-104">Actualiza los datos del actual objeto [Recordset](recordset-object-ado.md) o la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md) de la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-104">Refreshes the data in the current [Recordset](recordset-object-ado.md) object, or [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, from the underlying database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d0b5-105">Syntax</span></span>

<span data-ttu-id="5d0b5-106">*Conjunto de registros*. Resync*AffectRecords*, *ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="5d0b5-106">*Recordset*.Resync*AffectRecords*, *ResyncValues*</span></span>

<span data-ttu-id="5d0b5-107">*Registro*.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-107">*Record*.</span></span> <span data-ttu-id="5d0b5-108">*Los campos*. Resync*ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="5d0b5-108">*Fields*.Resync*ResyncValues*</span></span>

## <a name="parameters"></a><span data-ttu-id="5d0b5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d0b5-109">Parameters</span></span>

|<span data-ttu-id="5d0b5-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5d0b5-110">Parameter</span></span>|<span data-ttu-id="5d0b5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d0b5-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5d0b5-112">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="5d0b5-112">*AffectRecords*</span></span> |<span data-ttu-id="5d0b5-p102">Es opcional. Un valor de [AffectEnum](affectenum.md) que determina el número de registros que se verán afectados por el método **Resync**. El valor predeterminado es **adAffectAll**. Este valor no está disponible con el método **Resync** de la colección **Fields** de un objeto **Record**.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p102">Optional. An [AffectEnum](affectenum.md) value that determines how many records the **Resync** method will affect. The default value is **adAffectAll**. This value is not available with the **Resync** method of the **Fields** collection of a **Record** object.</span></span>|
|<span data-ttu-id="5d0b5-117">*Valor de ResyncValues*</span><span class="sxs-lookup"><span data-stu-id="5d0b5-117">*ResyncValues*</span></span> |<span data-ttu-id="5d0b5-p103">Es opcional. Un valor de [ResyncEnum](resyncenum.md) que especifica si se sobrescriben los valores subyacentes. El valor predeterminado es **adResyncAllValues**.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p103">Optional. A [ResyncEnum](resyncenum.md) value that specifies whether underlying values are overwritten. The default value is **adResyncAllValues**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5d0b5-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5d0b5-121">Remarks</span></span>

### <a name="recordset"></a><span data-ttu-id="5d0b5-122">Recordset</span><span class="sxs-lookup"><span data-stu-id="5d0b5-122">Recordset</span></span>

<span data-ttu-id="5d0b5-p104">Use el método **Resync** para volver a sincronizar los registros del actual objeto **Recordset** con la base de datos subyacente. Esto es útil si está usando un cursor estático o de solo avance, pero desea ver todos los cambios en la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p104">Use the **Resync** method to resynchronize records in the current **Recordset** with the underlying database. This is useful if you are using either a static or forward-only cursor, but you want to see any changes in the underlying database.</span></span>

<span data-ttu-id="5d0b5-125">Si establece el valor de la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient**, **Resync** solo está disponible para los objetos **Recordset** que no sean de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-125">If you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**, **Resync** is only available for non-read-only **Recordset** objects.</span></span>

<span data-ttu-id="5d0b5-p105">A diferencia del método [Requery](requery-method-ado.md), el método **Resync** no vuelve a ejecutar el comando subyacente del objeto **Recordset**. No se verán los nuevos registros de la base de datos subyacente.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p105">Unlike the [Requery](requery-method-ado.md) method, the **Resync** method does not re-execute the **Recordset** object's underlying command. New records in the underlying database will not be visible.</span></span>

<span data-ttu-id="5d0b5-p106">Si un intento de volver a sincronizar genera un error debido a un conflicto con los datos subyacentes (por ejemplo, un registro ha sido eliminado por otro usuario), el proveedor devuelve advertencias a la colección [Errors](errors-collection-ado.md) y se produce un error en tiempo de ejecución. Utilice la propiedad [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) y la propiedad [Status](status-property-ado-recordset.md) para localizar los registros con conflictos.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p106">If the attempt to resynchronize fails because of a conflict with the underlying data (for example, a record has been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection and a run-time error occurs. Use the [Filter](filter-property-ado.md) property (**adFilterConflictingRecords**) and the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="5d0b5-130">Si están establecidas las propiedades dinámicas [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y [Resync Command](resync-command-property-dynamic-ado.md), y si el objeto **Recordset** es el resultado de ejecutar una operación de JOIN en varias tablas, el método **Resync** ejecutará el comando especificado en la propiedad **Resync Command** sólo en la tabla indicada en la propiedad **Unique Table**.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-130">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and [Resync Command](resync-command-property-dynamic-ado.md) dynamic properties are set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Resync** method will execute the command given in the **Resync Command** property only on the table named in the **Unique Table** property.</span></span>

### <a name="fields"></a><span data-ttu-id="5d0b5-131">Campos</span><span class="sxs-lookup"><span data-stu-id="5d0b5-131">Fields</span></span>

<span data-ttu-id="5d0b5-p107">Utilice el método **Resync** para volver a sincronizar los valores de la colección **Fields** de un objeto **Record** con el origen de datos subyacente. Este método no afecta a la propiedad [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p107">Use the **Resync** method to resynchronize the values of the **Fields** collection of a **Record** object with the underlying data source. The [Count](count-property-ado.md) property is not affected by this method.</span></span>

<span data-ttu-id="5d0b5-134">Si el *valor de ResyncValues* está establecido en **adResyncAllValues** (valor predeterminado), se sincronizan los [UnderlyingValue](underlyingvalue-property-ado.md), [valor](value-property-ado.md)y las propiedades [OriginalValue](originalvalue-property-ado.md) de los objetos [Field](field-object-ado.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-134">If *ResyncValues* is set to **adResyncAllValues** (the default value), then the [UnderlyingValue](underlyingvalue-property-ado.md), [Value](value-property-ado.md), and [OriginalValue](originalvalue-property-ado.md) properties of [Field](field-object-ado.md) objects in the collection are synchronized.</span></span> <span data-ttu-id="5d0b5-135">Si el *valor de ResyncValues* está establecido en **adResyncUnderlyingValues**, sólo la propiedad **UnderlyingValue** está sincronizada.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-135">If *ResyncValues* is set to **adResyncUnderlyingValues**, only the **UnderlyingValue** property is synchronized.</span></span>

<span data-ttu-id="5d0b5-p109">El valor de la propiedad **Status** de cada objeto **Field** en el momento de la llamada también afecta al comportamiento de **Resync**. Para los objetos **Field** cuyo valor de **Status** es **adFieldPendingUnknown** o **adFieldPendingInsert**, **Resync** no tiene ningún efecto. Si **Status** tiene el valor **adFieldPendingChange** o **adFieldPendingDelete**, **Resync** sincroniza los valores de datos de los campos aún existentes en el origen de datos.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p109">The value of the **Status** property for each **Field** object at the time of the call also affects the behavior of **Resync**. For **Field** objects with **Status** values of **adFieldPendingUnknown** or **adFieldPendingInsert**, **Resync** has no effect. For **Status** values of **adFieldPendingChange** or **adFieldPendingDelete**, **Resync** synchronizes data values for fields that still exist at the data source.</span></span>

<span data-ttu-id="5d0b5-p110">**Resync** no modificará los valores de **Status** de los objetos **Field**, a menos que se produzca un error al llamar a **Resync**. Por ejemplo, si ya no existe el campo, el proveedor devolverá un valor de **Status** apropiado para el objeto **Field**, como **adFieldDoesNotExist**. Los valores devueltos de **Status** pueden combinarse lógicamente dentro del valor de la propiedad **Status**.</span><span class="sxs-lookup"><span data-stu-id="5d0b5-p110">**Resync** will not modify **Status** values of **Field** objects unless an error occurs when **Resync** is called. For example, if the field no longer exists, the provider will return an appropriate **Status** value for the **Field** object, such as **adFieldDoesNotExist**. Returned **Status** values may be logically combined within the value of the **Status** property.</span></span>

