---
title: FetchComplete (evento, ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293192"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="fb10d-102">FetchComplete (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="fb10d-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="fb10d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb10d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb10d-104">Al evento **FetchComplete** se le llama después de que todos los registros en una operación asincrónica prolongada se hayan recuperado e insertado en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fb10d-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb10d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb10d-105">Syntax</span></span>

<span data-ttu-id="fb10d-106">FetchComplete*perror*, \*\* adStatus, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="fb10d-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="fb10d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb10d-107">Parameters</span></span>

|<span data-ttu-id="fb10d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb10d-108">Parameter</span></span>|<span data-ttu-id="fb10d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb10d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fb10d-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="fb10d-110">*pError*</span></span> |<span data-ttu-id="fb10d-p101">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fb10d-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="fb10d-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="fb10d-113">*adStatus*</span></span> |<span data-ttu-id="fb10d-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="fb10d-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="fb10d-115">Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fb10d-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="fb10d-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="fb10d-116">*pRecordset*</span></span> |<span data-ttu-id="fb10d-p103">Objeto **Recordset**. El objeto para el que se recuperaron los registros.</span><span class="sxs-lookup"><span data-stu-id="fb10d-p103">A **Recordset** object. The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fb10d-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb10d-119">Remarks</span></span>

<span data-ttu-id="fb10d-120">Para utilizar **FetchComplete** con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="fb10d-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

