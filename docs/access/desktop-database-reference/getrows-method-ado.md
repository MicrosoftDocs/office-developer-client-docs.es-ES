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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292226"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="ed6b5-102">GetRows (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="ed6b5-102">GetRows method (ADO)</span></span>

<span data-ttu-id="ed6b5-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed6b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed6b5-104">Recupera varios registros de un objeto [Recordset](recordset-object-ado.md) en una matriz.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed6b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed6b5-105">Syntax</span></span>

<span data-ttu-id="ed6b5-106">\*\* = *conjunto de registros*de matriz. GetRows (*filas*, *Start*, *Fields* )</span><span class="sxs-lookup"><span data-stu-id="ed6b5-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="ed6b5-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed6b5-107">Return value</span></span>

<span data-ttu-id="ed6b5-108">Devuelve un valor de tipo **Variant** que es una matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed6b5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed6b5-109">Parameters</span></span>

|<span data-ttu-id="ed6b5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed6b5-110">Parameter</span></span>|<span data-ttu-id="ed6b5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed6b5-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ed6b5-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="ed6b5-112">*Rows*</span></span> |<span data-ttu-id="ed6b5-p101">Es opcional. Valor de [GetRowsOptionEnum](getrowsoptionenum.md) que indica el número de registros que se van a recuperar. El valor predeterminado es **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="ed6b5-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="ed6b5-116">*Start*</span></span> |<span data-ttu-id="ed6b5-p102">Es opcional. Valor de tipo **String** o **Variant** que se establece en el marcador del registro donde debe iniciar la operación de **GetRows**. También puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="ed6b5-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="ed6b5-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="ed6b5-120">*Fields*</span></span> |<span data-ttu-id="ed6b5-p103">Es opcional. **Variant** que representa el nombre o la posición ordinal de un solo campo, o bien, una matriz de nombres de campo o números de posición ordinal. ADO devuelve sólo los datos de estos campos.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ed6b5-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ed6b5-124">Remarks</span></span>

<span data-ttu-id="ed6b5-p104">Use el método **GetRows** para copiar los registros de un objeto **Recordset** a una matriz bidimensional. El primer subíndice identifica el campo y el segundo identifica el número de registro. La variable de *matriz* se ajusta automáticamente al tamaño correcto cuando el método **GetRows** devuelve los datos.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-p104">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array. The first subscript identifies the field and the second identifies the record number. The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="ed6b5-p105">Si no especifica un valor para el argumento *Rows*, el método **GetRows** recupera automáticamente todos los registros del objeto **Recordset**. Si solicita más registros de los que están disponibles, **GetRows** devuelve sólo el número de registros disponibles.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-p105">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object. If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="ed6b5-130">Si el objeto **Recordset** admite marcadores, puede especificar en qué registro el método **GetRows** debe comenzar a recuperar datos pasando el valor de la propiedad [Bookmark](bookmark-property-ado.md) de ese registro en el argumento *Start*.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="ed6b5-131">Si desea restringir los campos que debe devolver la llamada a **GetRows**, puede pasar el número o el nombre de un solo campo, o bien, una matriz de números y nombres de campo en el argumento *Fields*.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="ed6b5-132">Tras llamar a **GetRows**, el siguiente registro sin leer se convierte en el registro actual, o bien, el valor de la propiedad [EOF](bof-eof-properties-ado.md) se establece en **True** si no quedan registros.</span><span class="sxs-lookup"><span data-stu-id="ed6b5-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

