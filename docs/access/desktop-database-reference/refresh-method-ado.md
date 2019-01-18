---
title: Refresh (método, ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bd7c47e7c3e41a7b42571043cfafc9e4e909a9f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710590"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="9f18d-102">Refresh (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="9f18d-102">Refresh method (ADO)</span></span>

<span data-ttu-id="9f18d-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9f18d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9f18d-104">Actualiza los objetos de una colección para reflejar los objetos disponibles y específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9f18d-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f18d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f18d-105">Syntax</span></span>

<span data-ttu-id="9f18d-106">*colección*. Actualización</span><span class="sxs-lookup"><span data-stu-id="9f18d-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="9f18d-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f18d-107">Remarks</span></span>

<span data-ttu-id="9f18d-108">El método **Refresh** realiza diferentes tareas según la colección desde la que se llame al método.</span><span class="sxs-lookup"><span data-stu-id="9f18d-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f18d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f18d-109">Parameters</span></span>

<span data-ttu-id="9f18d-p101">Si se usa el método **Refresh** en la colección [Parameters](command-object-ado.md) de un objeto [Command](parameters-collection-ado.md), se recupera la información de parámetros del proveedor para el procedimiento almacenado o la consulta parametrizada especificada en el objeto **Command**. La colección estará vacía para los proveedores que no admitan llamadas a procedimientos almacenados o consultas parametrizadas.</span><span class="sxs-lookup"><span data-stu-id="9f18d-p101">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object. The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="9f18d-112">La propiedad [ActiveConnection](activeconnection-property-ado.md) del objeto **Command** debe establecerse en un objeto [Connection](connection-object-ado.md) válido, la propiedad [CommandText](commandtext-property-ado.md) en un comando válido y la propiedad [CommandType](commandtype-property-ado.md) en **adCmdStoredProc** antes de llamar al método **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="9f18d-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="9f18d-113">Si obtiene acceso a la colección **Parameters** antes de llamar al método **Refresh**, ADO llamará automáticamente al método y rellenará la colección.</span><span class="sxs-lookup"><span data-stu-id="9f18d-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

> [!NOTE]
> <span data-ttu-id="9f18d-p102">[!NOTA] Si utiliza el método **Refresh** para obtener información de parámetros del proveedor y se devuelve uno o varios objetos [Parameter](parameter-object-ado.md) de longitud variable, puede que ADO asigne memoria para los parámetros en función de su posible tamaño máximo, lo que provocará un error durante la ejecución. Debe establecer explícitamente la propiedad [Size](size-property-ado.md) de estos parámetros antes de llamar al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) para evitar errores.</span><span class="sxs-lookup"><span data-stu-id="9f18d-p102">If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.</span></span>

### <a name="fields"></a><span data-ttu-id="9f18d-116">Campos</span><span class="sxs-lookup"><span data-stu-id="9f18d-116">Fields</span></span>

<span data-ttu-id="9f18d-p103">Utilizar el método **Refresh** en la colección **Fields** no tiene ningún efecto visible. Para recuperar los cambios de la estructura de base de datos subyacente, debe utilizar el método [Requery](requery-method-ado.md) o, si el objeto [Recordset](recordset-object-ado.md) no admite marcadores, el método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9f18d-p103">Using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

### <a name="properties"></a><span data-ttu-id="9f18d-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f18d-119">Properties</span></span>

<span data-ttu-id="9f18d-p104">Si utiliza el método **Refresh** en una colección **Properties** de algunos objetos, se rellena la colección con las propiedades dinámicas que expone el proveedor. Estas propiedades proporcionan información acerca de la funcionalidad específica del proveedor, aparte de las propiedades integradas que ADO admite.</span><span class="sxs-lookup"><span data-stu-id="9f18d-p104">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes. These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

