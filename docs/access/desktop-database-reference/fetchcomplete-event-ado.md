---
title: FetchComplete (evento, ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 299fec4a831bbde5d3fd2d58e0f76edb2acea0f8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485403"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="09de9-102">FetchComplete (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="09de9-102">FetchComplete Event (ADO)</span></span>


<span data-ttu-id="09de9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="09de9-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="09de9-104">Al evento **FetchComplete** se le llama después de que todos los registros en una operación asincrónica prolongada se hayan recuperado e insertado en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="09de9-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09de9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09de9-105">Syntax</span></span>

<span data-ttu-id="09de9-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="09de9-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="09de9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09de9-107">Parameters</span></span>

  - <span data-ttu-id="09de9-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="09de9-108">*pError*</span></span>

  - <span data-ttu-id="09de9-p101">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="09de9-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="09de9-111">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="09de9-111">*adStatus*</span></span>

  - [<span data-ttu-id="09de9-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="09de9-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="09de9-113">Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="09de9-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="09de9-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="09de9-114">*pRecordset*</span></span>

  - <span data-ttu-id="09de9-p102">Objeto **Recordset**. El objeto para el que se recuperaron los registros.</span><span class="sxs-lookup"><span data-stu-id="09de9-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="09de9-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09de9-117">Remarks</span></span>

<span data-ttu-id="09de9-118">Para utilizar **FetchComplete** con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="09de9-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>
