---
title: GetRows (método, ADO)
TOCTitle: GetRows Method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc82a753adb5e9bd7a5a5d46b6ae8ce284a94375
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483566"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="d31e1-102">GetRows (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="d31e1-102">GetRows Method (ADO)</span></span>


<span data-ttu-id="d31e1-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d31e1-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="d31e1-104">Recupera varios registros de un objeto [Recordset](recordset-object-ado.md) en una matriz.</span><span class="sxs-lookup"><span data-stu-id="d31e1-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d31e1-105">Syntax</span></span>

<span data-ttu-id="d31e1-106">*matriz* = *conjunto de registros*. GetRows (*filas*, *Iniciar*, *campos* )</span><span class="sxs-lookup"><span data-stu-id="d31e1-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="d31e1-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d31e1-107">Return Value</span></span>

<span data-ttu-id="d31e1-108">Devuelve un valor de tipo **Variant** que es una matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="d31e1-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="d31e1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d31e1-109">Parameters</span></span>

  - <span data-ttu-id="d31e1-110">*Rows*</span><span class="sxs-lookup"><span data-stu-id="d31e1-110">*Rows*</span></span>

  - <span data-ttu-id="d31e1-p101">Es opcional. Valor de [GetRowsOptionEnum](getrowsoptionenum.md) que indica el número de registros que se van a recuperar. El valor predeterminado es **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="d31e1-p101">Optional. A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve. The default is **adGetRowsRest**.</span></span>

  - <span data-ttu-id="d31e1-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="d31e1-114">*Start*</span></span>

  - <span data-ttu-id="d31e1-p102">Es opcional. Valor de tipo **String** o **Variant** que se establece en el marcador del registro donde debe iniciar la operación de **GetRows**. También puede utilizar un valor de [BookmarkEnum](bookmarkenum.md).</span><span class="sxs-lookup"><span data-stu-id="d31e1-p102">Optional. A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin. You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

  - <span data-ttu-id="d31e1-118">*Fields*</span><span class="sxs-lookup"><span data-stu-id="d31e1-118">*Fields*</span></span>

  - <span data-ttu-id="d31e1-p103">Es opcional. **Variant** que representa el nombre o la posición ordinal de un solo campo, o bien, una matriz de nombres de campo o números de posición ordinal. ADO devuelve sólo los datos de estos campos.</span><span class="sxs-lookup"><span data-stu-id="d31e1-p103">Optional. A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers. ADO returns only the data in these fields.</span></span>

## <a name="remarks"></a><span data-ttu-id="d31e1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d31e1-122">Remarks</span></span>

<span data-ttu-id="d31e1-123">Use el método **GetRows** para copiar los registros de un objeto **Recordset** a una matriz bidimensional.</span><span class="sxs-lookup"><span data-stu-id="d31e1-123">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="d31e1-124">El primer subíndice identifica el campo y el segundo identifica el número de registro.</span><span class="sxs-lookup"><span data-stu-id="d31e1-124">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="d31e1-125">La variable de *matriz* se ajusta automáticamente al tamaño correcto cuando el método **GetRows** devuelve los datos.</span><span class="sxs-lookup"><span data-stu-id="d31e1-125">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="d31e1-126">Si no especifica un valor para el argumento *Rows* , el método **GetRows** recupera automáticamente todos los registros en el objeto **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d31e1-126">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="d31e1-127">Si solicita más registros de los que están disponibles, **GetRows** devuelve sólo el número de registros disponibles.</span><span class="sxs-lookup"><span data-stu-id="d31e1-127">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="d31e1-128">Si el objeto **Recordset** admite marcadores, puede especificar en qué registro el método **GetRows** debe comenzar a recuperar datos pasando el valor de propiedad de [Bookmark](bookmark-property-ado.md) de ese registro en el argumento *Start* .</span><span class="sxs-lookup"><span data-stu-id="d31e1-128">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="d31e1-129">Si desea restringir los campos que devuelve la llamada a **GetRows** , puede pasar un nombre o número del campo único o una matriz de números y nombres de campo en el argumento *Fields* .</span><span class="sxs-lookup"><span data-stu-id="d31e1-129">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="d31e1-130">Tras llamar a **GetRows**, el siguiente registro sin leer se convierte en el registro actual, o bien, el valor de la propiedad [EOF](bof-eof-properties-ado.md) se establece en **True** si no quedan registros.</span><span class="sxs-lookup"><span data-stu-id="d31e1-130">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>

