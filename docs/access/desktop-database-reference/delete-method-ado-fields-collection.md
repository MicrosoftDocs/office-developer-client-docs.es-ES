---
title: Delete (método, colección Fields de ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fc2e614916026effe6ee0a9766e0b23db200574
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886399"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="ad33a-102">Delete (método, colección Fields de ADO)</span><span class="sxs-lookup"><span data-stu-id="ad33a-102">Delete Method (ADO Fields Collection)</span></span>


<span data-ttu-id="ad33a-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad33a-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="ad33a-104">Elimina un objeto de la colección [Fields](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ad33a-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad33a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad33a-105">Syntax</span></span>

<span data-ttu-id="ad33a-106">*Los campos*. Eliminar*campo*</span><span class="sxs-lookup"><span data-stu-id="ad33a-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="ad33a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad33a-107">Parameters</span></span>

  - <span data-ttu-id="ad33a-108">*Field*</span><span class="sxs-lookup"><span data-stu-id="ad33a-108">*Field*</span></span>

  - <span data-ttu-id="ad33a-p101">**Variant** que designa el objeto [Field](field-object-ado.md) que se va a eliminar. Este parámetro puede ser el nombre del objeto **Field** o la posición ordinal del objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="ad33a-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad33a-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ad33a-111">Remarks</span></span>

<span data-ttu-id="ad33a-112">Si se llama al método **Fields.Delete** en un objeto [Recordset](recordset-object-ado.md) abierto, se provoca un error de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ad33a-112">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

