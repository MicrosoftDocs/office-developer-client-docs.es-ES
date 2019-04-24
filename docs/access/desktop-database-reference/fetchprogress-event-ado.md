---
title: FetchProgress (evento, ADO)
TOCTitle: FetchProgress event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d863f51e7836acdc577ecd720df77114ed66f067
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293185"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="e7a78-102">FetchProgress (evento, ADO)</span><span class="sxs-lookup"><span data-stu-id="e7a78-102">FetchProgress event (ADO)</span></span>

<span data-ttu-id="e7a78-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7a78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7a78-104">Al evento **FetchProgress** se le llama periódicamente durante una operación asincrónica prolongada para informar de cuántas filas se han recuperado e insertado actualmente en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e7a78-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a78-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7a78-105">Syntax</span></span>

<span data-ttu-id="e7a78-106">FetchProgress\*\* Progress, *MaxProgress*, adStatus, *pRecordset* \*\*</span><span class="sxs-lookup"><span data-stu-id="e7a78-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="e7a78-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7a78-107">Parameters</span></span>

|<span data-ttu-id="e7a78-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7a78-108">Parameter</span></span>|<span data-ttu-id="e7a78-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7a78-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e7a78-110">*Progress*</span><span class="sxs-lookup"><span data-stu-id="e7a78-110">*Progress*</span></span> |<span data-ttu-id="e7a78-111">Valor **Long** que indica el número de registros que han sido recuperados actualmente por la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e7a78-111">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>|
|<span data-ttu-id="e7a78-112">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="e7a78-112">*MaxProgress*</span></span> |<span data-ttu-id="e7a78-113">Valor **Long** que indica el número máximo de registros que se espera recuperar.</span><span class="sxs-lookup"><span data-stu-id="e7a78-113">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>|
|<span data-ttu-id="e7a78-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="e7a78-114">*adStatus*</span></span> |<span data-ttu-id="e7a78-115">Valor de estado [EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="e7a78-115">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>|
|<span data-ttu-id="e7a78-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="e7a78-116">*pRecordset*</span></span> |<span data-ttu-id="e7a78-117">Objeto **Recordset** para el que se están recuperando los registros.</span><span class="sxs-lookup"><span data-stu-id="e7a78-117">A **Recordset** object that is the object for which the records are being retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e7a78-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7a78-118">Remarks</span></span>

<span data-ttu-id="e7a78-p101">Cuando use **FetchProgress** con un objeto **Recordset** secundario, tenga en cuenta que los valores de los parámetros *Progress* y *MaxProgress* se obtienen del conjunto de filas del [Servicio de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md) subyacente. Los valores devueltos representan el número total de registros en el conjunto de filas subyacente, no solo el número de registros en el capítulo actual.</span><span class="sxs-lookup"><span data-stu-id="e7a78-p101">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset. The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>

> [!NOTE]
> <span data-ttu-id="e7a78-121">[!NOTA] Para utilizar **FetchProgress** con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="e7a78-121">To use **FetchProgress** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>


