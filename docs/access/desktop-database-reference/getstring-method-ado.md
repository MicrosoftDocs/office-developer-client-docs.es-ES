---
title: Método GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292191"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="7a7de-102">Método GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="7a7de-102">GetString method (ADO)</span></span>

<span data-ttu-id="7a7de-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a7de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a7de-104">Devuelve el objeto [Recordset](recordset-object-ado.md) en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="7a7de-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a7de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a7de-105">Syntax</span></span>

<span data-ttu-id="7a7de-106">*Variant*  =  *recordset*. GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="7a7de-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="7a7de-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a7de-107">Return value</span></span>

<span data-ttu-id="7a7de-108">Devuelve el objeto **Recordset** como **Variant** de valores de cadena (BSTR).</span><span class="sxs-lookup"><span data-stu-id="7a7de-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="7a7de-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a7de-109">Parameters</span></span>

|<span data-ttu-id="7a7de-110">Parámetro</span><span class="sxs-lookup"><span data-stu-id="7a7de-110">Parameter</span></span>|<span data-ttu-id="7a7de-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a7de-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="7a7de-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="7a7de-112">*StringFormat*</span></span> |<span data-ttu-id="7a7de-p101">Valor de [StringFormatEnum](stringformatenum.md) que especifica cómo debe convertirse el objeto **Recordset** en una cadena. Los parámetros *RowDelimiter*, *ColumnDelimiter* y *NullExpr* se utilizan sólo cuando el valor de *StringFormat* es **adClipString**.</span><span class="sxs-lookup"><span data-stu-id="7a7de-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="7a7de-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="7a7de-115">*NumRows*</span></span> |<span data-ttu-id="7a7de-p102">Es opcional. Número de filas del objeto **Recordset** que se van a convertir. Si no se especifica *NumRows* o si es mayor que el número total de filas en el objeto **Recordset**, se convertirán todas las filas del objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7a7de-p102">Optional. The number of rows to be converted in the **Recordset**. If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="7a7de-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="7a7de-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="7a7de-p103">Es opcional. Delimitador que se utiliza entre las columnas, si se ha especificado; en caso contrario, el carácter de tabulación.</span><span class="sxs-lookup"><span data-stu-id="7a7de-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="7a7de-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="7a7de-122">*RowDelimiter*</span></span> |<span data-ttu-id="7a7de-p104">Es opcional. Delimitador que se utiliza entre las filas, si se ha especificado; en caso contrario, el carácter de retorno de carro.</span><span class="sxs-lookup"><span data-stu-id="7a7de-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="7a7de-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="7a7de-125">*NullExpr*</span></span> |<span data-ttu-id="7a7de-p105">Es opcional. Expresión que se utiliza en lugar de un valor nulo, si se ha especificado; en caso contrario, la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="7a7de-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7a7de-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a7de-128">Remarks</span></span>

<span data-ttu-id="7a7de-p106">En la cadena se guardan los datos de fila y no los datos de esquema. Por lo tanto, no se puede volver a abrir un objeto **Recordset** mediante esta cadena.</span><span class="sxs-lookup"><span data-stu-id="7a7de-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="7a7de-131">Este método es equivalente al método **GetClipString** de RDO.</span><span class="sxs-lookup"><span data-stu-id="7a7de-131">This method is equivalent to the RDO **GetClipString** method.</span></span>

