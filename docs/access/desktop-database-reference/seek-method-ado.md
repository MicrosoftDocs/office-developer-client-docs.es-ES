---
title: 'Método Seek: ActiveX Data Objects (ADO)'
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308795"
---
# <a name="seek-method-ado"></a><span data-ttu-id="defc6-102">Método Seek (ADO)</span><span class="sxs-lookup"><span data-stu-id="defc6-102">Seek method (ADO)</span></span>

<span data-ttu-id="defc6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="defc6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="defc6-104">Busca en el índice de un objeto [Recordset](recordset-object-ado.md) para localizar rápidamente la fila que coincida con los valores especificados, y cambia la posición de fila actual a dicha fila.</span><span class="sxs-lookup"><span data-stu-id="defc6-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="defc6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="defc6-105">Syntax</span></span>

<span data-ttu-id="defc6-106">*recordset*. Seek *KeyValues*, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="defc6-106">*recordset*.Seek *KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="defc6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="defc6-107">Parameters</span></span>

|<span data-ttu-id="defc6-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="defc6-108">Parameter</span></span>|<span data-ttu-id="defc6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="defc6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="defc6-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="defc6-110">*KeyValues*</span></span> |<span data-ttu-id="defc6-p101">Matriz de valores **Variant**. Un índice consta de una o varias columnas y la matriz contiene un valor que se va a comparar con cada columna correspondiente.</span><span class="sxs-lookup"><span data-stu-id="defc6-p101">An array of **Variant** values. An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="defc6-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="defc6-113">*SeekOption*</span></span> |<span data-ttu-id="defc6-114">Valor de [SeekEnum](seekenum.md) que especifica el tipo de comparación que se va a realizar entre las columnas del índice y el valor de *KeyValues* correspondiente.</span><span class="sxs-lookup"><span data-stu-id="defc6-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="defc6-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="defc6-115">Remarks</span></span>

<span data-ttu-id="defc6-p102">Use el método **Seek** junto con la propiedad [Index](index-property-ado.md) si el proveedor subyacente admite índices en el objeto **Recordset**. Use el método [Supports](supports-method-ado.md)**(adSeek)** para determinar si el proveedor subyacente admite **Seek**, y el método **Supports(adIndex)** para determinar si el proveedor admite índices. Por ejemplo, el [proveedor OLE DB para Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) admite **Seek** e **Index**.</span><span class="sxs-lookup"><span data-stu-id="defc6-p102">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="defc6-p103">Si **Seek** no encuentra la fila deseada, no se produce ningún error y la fila se coloca al final del objeto **Recordset**. Establezca la propiedad **Index** en el índice deseado antes de ejecutar este método.</span><span class="sxs-lookup"><span data-stu-id="defc6-p103">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="defc6-p104">Este método se puede usar sólo con cursores de servidor. Seek no se admite cuando el valor de la propiedad **CursorLocation** del objeto [Recordset](cursorlocation-property-ado.md) es **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="defc6-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="defc6-123">Este método se puede usar únicamente cuando el objeto **Recordset** se ha abierto con un valor [adCmdTableDirect](commandtypeenum.md) de **CommandTypeEnum**.</span><span class="sxs-lookup"><span data-stu-id="defc6-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

