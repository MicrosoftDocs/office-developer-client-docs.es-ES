---
title: FetchComplete (evento, ADO)
TOCTitle: FetchComplete Event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e4b72bb3e05b4ef05358a80faffaa0ee4ce08a80
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882402"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="3c3f7-102">FetchComplete (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="3c3f7-102">FetchComplete Event (ADO)</span></span>


<span data-ttu-id="3c3f7-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c3f7-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3c3f7-104">Al evento **FetchComplete** se le llama después de que todos los registros en una operación asincrónica prolongada se hayan recuperado e insertado en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3c3f7-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c3f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c3f7-105">Syntax</span></span>

<span data-ttu-id="3c3f7-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="3c3f7-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="3c3f7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c3f7-107">Parameters</span></span>

  - <span data-ttu-id="3c3f7-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="3c3f7-108">*pError*</span></span>

  - <span data-ttu-id="3c3f7-p101">Objeto [Error](error-object-ado.md). Describe el error que se produjo si el valor de **adStatus** es **adStatusErrorsOccurred**; de lo contrario, no se establece ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3c3f7-p101">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="3c3f7-111">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="3c3f7-111">*adStatus*</span></span>

  - [<span data-ttu-id="3c3f7-112">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="3c3f7-112">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="3c3f7-113">Antes de que el evento vuelva, establezca este parámetro en **adStatusUnwantedEvent** para impedir notificaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3c3f7-113">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="3c3f7-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="3c3f7-114">*pRecordset*</span></span>

  - <span data-ttu-id="3c3f7-p102">Objeto **Recordset**. El objeto para el que se recuperaron los registros.</span><span class="sxs-lookup"><span data-stu-id="3c3f7-p102">A **Recordset** object. The object for which the records were retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c3f7-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3c3f7-117">Remarks</span></span>

<span data-ttu-id="3c3f7-118">Para utilizar **FetchComplete** con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="3c3f7-118">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

