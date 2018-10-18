---
title: GetString (método, ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba235094aa7f491cbd86bf753713d50f01009d47
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605404"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="6b81a-102">GetString (método, ADO)</span><span class="sxs-lookup"><span data-stu-id="6b81a-102">GetString Method (ADO)</span></span>


<span data-ttu-id="6b81a-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b81a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6b81a-104">Devuelve el objeto [Recordset](recordset-object-ado.md) en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="6b81a-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b81a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b81a-105">Syntax</span></span>

<span data-ttu-id="6b81a-106">*Variant* = *conjunto de registros*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="6b81a-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

<span data-ttu-id="6b81a-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6b81a-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="6b81a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b81a-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="6b81a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b81a-109">Return value</span></span>
>>>>>>> <span data-ttu-id="6b81a-110">master</span><span class="sxs-lookup"><span data-stu-id="6b81a-110">master</span></span>

<span data-ttu-id="6b81a-111">Devuelve el objeto **Recordset** como **Variant** de valores de cadena (BSTR).</span><span class="sxs-lookup"><span data-stu-id="6b81a-111">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="6b81a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b81a-112">Parameters</span></span>

  - <span data-ttu-id="6b81a-113">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="6b81a-113">*StringFormat*</span></span>

  - <span data-ttu-id="6b81a-p101">Valor de [StringFormatEnum](stringformatenum.md) que especifica cómo debe convertirse el objeto **Recordset** en una cadena. Los parámetros *RowDelimiter*, *ColumnDelimiter* y *NullExpr* se utilizan sólo cuando el valor de *StringFormat* es **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="6b81a-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="6b81a-116">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="6b81a-116">*NumRows*</span></span>

  - <span data-ttu-id="6b81a-117">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="6b81a-117">Optional.</span></span> <span data-ttu-id="6b81a-118">Número de filas del objeto **Recordset** que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="6b81a-118">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="6b81a-119">Si no se especifica *NumRows* o si es mayor que el número total de filas en el **conjunto de registros**, a continuación, se convierten todas las filas en el **conjunto de registros** .</span><span class="sxs-lookup"><span data-stu-id="6b81a-119">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="6b81a-120">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="6b81a-120">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="6b81a-p103">Es opcional. Delimitador que se utiliza entre las columnas, si se ha especificado; en caso contrario, el carácter de tabulación.</span><span class="sxs-lookup"><span data-stu-id="6b81a-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="6b81a-123">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="6b81a-123">*RowDelimiter*</span></span>

  - <span data-ttu-id="6b81a-p104">Es opcional. Delimitador que se utiliza entre las filas, si se ha especificado; en caso contrario, el carácter de retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="6b81a-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="6b81a-126">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="6b81a-126">*NullExpr*</span></span>

  - <span data-ttu-id="6b81a-p105">Es opcional. Expresión que se utiliza en lugar de un valor nulo, si se ha especificado; en caso contrario, la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="6b81a-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b81a-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b81a-129">Remarks</span></span>

<span data-ttu-id="6b81a-p106">En la cadena se guardan los datos de fila y no los datos de esquema. Por lo tanto, no se puede volver a abrir un objeto **Recordset** mediante esta cadena.</span><span class="sxs-lookup"><span data-stu-id="6b81a-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="6b81a-132">Este método es equivalente al método **GetClipString** de RDO.</span><span class="sxs-lookup"><span data-stu-id="6b81a-132">This method is equivalent to the RDO **GetClipString** method.</span></span>

