---
title: Requery (método, ADO)
TOCTitle: Requery method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 249dc236d730cf773ec38fe5dd903cb64ca9b594
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705683"
---
# <a name="requery-method-ado"></a><span data-ttu-id="7b4a7-102">Requery (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="7b4a7-102">Requery method (ADO)</span></span>

<span data-ttu-id="7b4a7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b4a7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b4a7-104">Actualiza los datos de un objeto [Recordset](recordset-object-ado.md) ejecutando de nuevo la consulta en la que se basa el objeto.</span><span class="sxs-lookup"><span data-stu-id="7b4a7-104">Updates the data in a [Recordset](recordset-object-ado.md) object by re-executing the query on which the object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b4a7-105">Syntax</span></span>

<span data-ttu-id="7b4a7-106">*conjunto de registros*. Requery *Opciones*</span><span class="sxs-lookup"><span data-stu-id="7b4a7-106">*recordset*.Requery *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="7b4a7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b4a7-107">Parameters</span></span>

|<span data-ttu-id="7b4a7-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="7b4a7-108">Name</span></span> |<span data-ttu-id="7b4a7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b4a7-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="7b4a7-110">*Options*</span><span class="sxs-lookup"><span data-stu-id="7b4a7-110">*Options*</span></span> |<span data-ttu-id="7b4a7-p101">Es opcional. Máscara de bits que contiene valores de [ExecuteOptionEnum](executeoptionenum.md) y [CommandTypeEnum](commandtypeenum.md) que afectan a esta operación.</span><span class="sxs-lookup"><span data-stu-id="7b4a7-p101">Optional. A bitmask that contains [ExecuteOptionEnum](executeoptionenum.md) and [CommandTypeEnum](commandtypeenum.md) values affecting this operation.</span></span>|

> [!NOTE]
> <span data-ttu-id="7b4a7-113">Si *las opciones* está establecido en **adAsyncExecute**, esta operación se ejecutará asincrónicamente y se emitirá un evento [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) cuando finalice.</span><span class="sxs-lookup"><span data-stu-id="7b4a7-113">If *Options* is set to **adAsyncExecute**, this operation will execute asynchronously and a [RecordsetChangeComplete](willchangerecordset-and-recordsetchangecomplete-events-ado.md) event will be issued when it concludes.</span></span>

<span data-ttu-id="7b4a7-114">Los valores de **ExecuteOpenEnum** de **adExecuteNoRecords** o **adExecuteStream** no deben utilizarse con **Requery**.</span><span class="sxs-lookup"><span data-stu-id="7b4a7-114">The **ExecuteOpenEnum** values of **adExecuteNoRecords** or **adExecuteStream** should not be used with **Requery**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b4a7-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b4a7-115">Remarks</span></span>

<span data-ttu-id="7b4a7-p102">Utilice el método **Requery** para actualizar todo el contenido de un objeto **Recordset** desde el origen de datos ejecutando de nuevo el comando original y recuperando los datos por segunda vez. Llamar a este método equivale a llamar sucesivamente a los métodos [Close](close-method-ado.md) y [Open](open-method-ado-recordset.md). Si está modificando el registro actual o agregando un registro nuevo, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="7b4a7-p102">Use the **Requery** method to refresh the entire contents of a **Recordset** object from the data source by reissuing the original command and retrieving the data a second time. Calling this method is equivalent to calling the [Close](close-method-ado.md) and [Open](open-method-ado-recordset.md) methods in succession. If you are editing the current record or adding a new record, an error occurs.</span></span>

<span data-ttu-id="7b4a7-p103">Mientras esté abierto el objeto **Recordset**, las propiedades que definen la naturaleza del cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), etc.) son de solo lectura. Por lo tanto, el método **Requery** solamente puede actualizar el cursor actual. Para cambiar alguna propiedad del cursor y ver los resultados, debe usar el método [Close](close-method-ado.md) para que las propiedades vuelvan a ser de lectura y escritura. A continuación, podrá cambiar los valores de configuración de las propiedades y llamar al método [Open](open-method-ado-recordset.md) para volver a abrir el cursor.</span><span class="sxs-lookup"><span data-stu-id="7b4a7-p103">While the **Recordset** object is open, the properties that define the nature of the cursor ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), and so forth) are read-only. Thus, the **Requery** method can only refresh the current cursor. To change any of the cursor properties and view the results, you must use the [Close](close-method-ado.md) method so that the properties become read/write again. You can then change the property settings and call the [Open](open-method-ado-recordset.md) method to reopen the cursor.</span></span>

