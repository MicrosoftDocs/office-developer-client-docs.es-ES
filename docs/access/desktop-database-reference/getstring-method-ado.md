---
title: GetString (método, ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698214"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="fe7b6-102">GetString (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="fe7b6-102">GetString method (ADO)</span></span>

<span data-ttu-id="fe7b6-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe7b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe7b6-104">Devuelve el objeto [Recordset](recordset-object-ado.md) en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe7b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe7b6-105">Syntax</span></span>

<span data-ttu-id="fe7b6-106">*Variant* = *conjunto de registros*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="fe7b6-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="fe7b6-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe7b6-107">Return value</span></span>

<span data-ttu-id="fe7b6-108">Devuelve el objeto **Recordset** como **Variant** de valores de cadena (BSTR).</span><span class="sxs-lookup"><span data-stu-id="fe7b6-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="fe7b6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe7b6-109">Parameters</span></span>

|<span data-ttu-id="fe7b6-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fe7b6-110">Parameter</span></span>|<span data-ttu-id="fe7b6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe7b6-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fe7b6-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="fe7b6-112">*StringFormat*</span></span> |<span data-ttu-id="fe7b6-p101">Valor de [StringFormatEnum](stringformatenum.md) que especifica cómo debe convertirse el objeto **Recordset** en una cadena. Los parámetros *RowDelimiter*, *ColumnDelimiter* y *NullExpr* se utilizan sólo cuando el valor de *StringFormat* es **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="fe7b6-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="fe7b6-115">*NumRows*</span></span> |<span data-ttu-id="fe7b6-116">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-116">Optional.</span></span> <span data-ttu-id="fe7b6-117">Número de filas del objeto **Recordset** que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="fe7b6-118">Si no se especifica *NumRows* o si es mayor que el número total de filas en el **conjunto de registros**, a continuación, se convierten todas las filas en el **conjunto de registros** .</span><span class="sxs-lookup"><span data-stu-id="fe7b6-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="fe7b6-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="fe7b6-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="fe7b6-p103">Es opcional. Delimitador que se utiliza entre las columnas, si se ha especificado; en caso contrario, el carácter de tabulación.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="fe7b6-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="fe7b6-122">*RowDelimiter*</span></span> |<span data-ttu-id="fe7b6-p104">Es opcional. Delimitador que se utiliza entre las filas, si se ha especificado; en caso contrario, el carácter de retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="fe7b6-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="fe7b6-125">*NullExpr*</span></span> |<span data-ttu-id="fe7b6-p105">Es opcional. Expresión que se utiliza en lugar de un valor nulo, si se ha especificado; en caso contrario, la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fe7b6-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe7b6-128">Remarks</span></span>

<span data-ttu-id="fe7b6-p106">En la cadena se guardan los datos de fila y no los datos de esquema. Por lo tanto, no se puede volver a abrir un objeto **Recordset** mediante esta cadena.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="fe7b6-131">Este método es equivalente al método **GetClipString** de RDO.</span><span class="sxs-lookup"><span data-stu-id="fe7b6-131">This method is equivalent to the RDO **GetClipString** method.</span></span>

