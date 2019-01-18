---
title: GetRows (método, ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f7ce441eb837b76e824b55393741e0cf821bb5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709631"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="c34a3-102">GetRows (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="c34a3-102">GetRows method (ADO)</span></span>

<span data-ttu-id="c34a3-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c34a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c34a3-104">Recupera varios registros de un objeto [Recordset](recordset-object-ado.md) en una matriz.</span><span class="sxs-lookup"><span data-stu-id="c34a3-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="c34a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c34a3-105">Syntax</span></span>

<span data-ttu-id="c34a3-106">*matriz* = *conjunto de registros*. GetRows (*filas*, *Iniciar*, *campos* )</span><span class="sxs-lookup"><span data-stu-id="c34a3-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="c34a3-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c34a3-107">Return value</span></span>

<span data-ttu-id="c34a3-108">Devuelve un valor de tipo **Variant** que es una matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="c34a3-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="c34a3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c34a3-109">Parameters</span></span>

|<span data-ttu-id="c34a3-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c34a3-110">Parameter</span></span>|<span data-ttu-id="c34a3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c34a3-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c34a3-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="c34a3-112">*Rows*</span></span> |<span data-ttu-id="c34a3-p101">Es opcional. Valor de [GetRowsOptionEnum](getrowsoptionenum.md) que indica el número de registros que se van a recuperar. El valor predeterminado es **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="c34a3-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="c34a3-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="c34a3-116">*Start*</span></span> |<span data-ttu-id="c34a3-p102">Es opcional. Valor de tipo **String** o **Variant** que se establece en el marcador del registro donde debe iniciar la operación de **GetRows**. También puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="c34a3-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="c34a3-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="c34a3-120">*Fields*</span></span> |<span data-ttu-id="c34a3-p103">Es opcional. **Variant** que representa el nombre o la posición ordinal de un solo campo, o bien, una matriz de nombres de campo o números de posición ordinal. ADO devuelve sólo los datos de estos campos.</span><span class="sxs-lookup"><span data-stu-id="c34a3-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c34a3-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c34a3-124">Remarks</span></span>

<span data-ttu-id="c34a3-125">Use el método **GetRows** para copiar los registros de un objeto **Recordset** a una matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="c34a3-125">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="c34a3-126">El primer subíndice identifica el campo y el segundo identifica el número de registro.</span><span class="sxs-lookup"><span data-stu-id="c34a3-126">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="c34a3-127">La variable de *matriz* se ajusta automáticamente al tamaño correcto cuando el método **GetRows** devuelve los datos.</span><span class="sxs-lookup"><span data-stu-id="c34a3-127">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="c34a3-128">Si no especifica un valor para el argumento *Rows* , el método **GetRows** recupera automáticamente todos los registros en el objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="c34a3-128">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="c34a3-129">Si solicita más registros de los que están disponibles, **GetRows** devuelve sólo el número de registros disponibles.</span><span class="sxs-lookup"><span data-stu-id="c34a3-129">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="c34a3-130">Si el objeto **Recordset** admite marcadores, puede especificar en qué registro el método **GetRows** debe comenzar a recuperar datos pasando el valor de propiedad de [Bookmark](bookmark-property-ado.md) de ese registro en el argumento *Start* .</span><span class="sxs-lookup"><span data-stu-id="c34a3-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="c34a3-131">Si desea restringir los campos que devuelve la llamada a **GetRows** , puede pasar un nombre o número del campo único o una matriz de números y nombres de campo en el argumento *Fields* .</span><span class="sxs-lookup"><span data-stu-id="c34a3-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="c34a3-132">Tras llamar a **GetRows**, el siguiente registro sin leer se convierte en el registro actual, o bien, el valor de la propiedad [EOF](bof-eof-properties-ado.md) se establece en **True** si no quedan registros.</span><span class="sxs-lookup"><span data-stu-id="c34a3-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

