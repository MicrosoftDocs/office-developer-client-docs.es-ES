---
title: Método Delete (colección de campos de ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718262"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="ceb8e-102">Método Delete (colección de campos de ADO)</span><span class="sxs-lookup"><span data-stu-id="ceb8e-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="ceb8e-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ceb8e-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ceb8e-104">Elimina un objeto de la colección [Fields](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ceb8e-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb8e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ceb8e-105">Syntax</span></span>

<span data-ttu-id="ceb8e-106">*Los campos*. Eliminar*campo*</span><span class="sxs-lookup"><span data-stu-id="ceb8e-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="ceb8e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ceb8e-107">Parameters</span></span>

|<span data-ttu-id="ceb8e-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="ceb8e-108">Parameter</span></span>|<span data-ttu-id="ceb8e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb8e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ceb8e-110">*Field*</span><span class="sxs-lookup"><span data-stu-id="ceb8e-110">*Field*</span></span> |<span data-ttu-id="ceb8e-p101">**Variant** que designa el objeto [Field](field-object-ado.md) que se va a eliminar. Este parámetro puede ser el nombre del objeto **Field** o la posición ordinal del objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="ceb8e-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ceb8e-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ceb8e-113">Remarks</span></span>

<span data-ttu-id="ceb8e-114">Si se llama al método **Fields.Delete** en un objeto [Recordset](recordset-object-ado.md) abierto, se provoca un error de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ceb8e-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

