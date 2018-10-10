---
title: FetchProgress (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72a860ecd52e0481b55423f88e537eab3c8de2ae
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485069"
---
# <a name="fetchprogress-event-ado"></a><span data-ttu-id="66bb6-102">FetchProgress (ADO)</span><span class="sxs-lookup"><span data-stu-id="66bb6-102">FetchProgress Event (ADO)</span></span>


<span data-ttu-id="66bb6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="66bb6-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="66bb6-104">Al evento **FetchProgress** se le llama periódicamente durante una operación asincrónica prolongada para informar de cuántas filas se han recuperado e insertado actualmente en el objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="66bb6-104">The **FetchProgress** event is called periodically during a lengthy asynchronous operation to report how many more rows have currently been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="66bb6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66bb6-105">Syntax</span></span>

<span data-ttu-id="66bb6-106">De*progreso*, *MaxProgress*, FetchProgress *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="66bb6-106">FetchProgress*Progress*, *MaxProgress*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="66bb6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66bb6-107">Parameters</span></span>

  - <span data-ttu-id="66bb6-108">*Progress*</span><span class="sxs-lookup"><span data-stu-id="66bb6-108">*Progress*</span></span>

  - <span data-ttu-id="66bb6-109">Valor **Long** que indica el número de registros que han sido recuperados actualmente por la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="66bb6-109">A **Long** value indicating the number of records that have currently been retrieved by the fetch operation.</span></span>

  - <span data-ttu-id="66bb6-110">*MaxProgress*</span><span class="sxs-lookup"><span data-stu-id="66bb6-110">*MaxProgress*</span></span>

  - <span data-ttu-id="66bb6-111">Valor **Long** que indica el número máximo de registros que se espera recuperar.</span><span class="sxs-lookup"><span data-stu-id="66bb6-111">A **Long** value indicating the maximum number of records expected to be retrieved.</span></span>

  - <span data-ttu-id="66bb6-112">*valor de adStatus*</span><span class="sxs-lookup"><span data-stu-id="66bb6-112">*adStatus*</span></span>

  - <span data-ttu-id="66bb6-113">Valor de estado [EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="66bb6-113">An [EventStatusEnum](eventstatusenum.md) status value.</span></span>

  - <span data-ttu-id="66bb6-114">*Connection*</span><span class="sxs-lookup"><span data-stu-id="66bb6-114">*pRecordset*</span></span>

  - <span data-ttu-id="66bb6-115">Objeto **Recordset** para el que se están recuperando los registros.</span><span class="sxs-lookup"><span data-stu-id="66bb6-115">A **Recordset** object that is the object for which the records are being retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="66bb6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66bb6-116">Remarks</span></span>

<span data-ttu-id="66bb6-117">Cuando utilice **FetchProgress** con un **Recordset**secundario, tenga en cuenta que los valores de parámetro *Progress* y *MaxProgress* se derivan del conjunto de filas subyacente [Del servicio de cursores](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="66bb6-117">When using **FetchProgress** with a child **Recordset**, be aware that the *Progress* and *MaxProgress* parameter values are derived from the underlying [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md) rowset.</span></span> <span data-ttu-id="66bb6-118">Los valores devueltos representan el número total de registros en el conjunto de filas subyacente, no solo el número de registros en el capítulo actual.</span><span class="sxs-lookup"><span data-stu-id="66bb6-118">The values returned represent the total number of records in the underlying rowset, not just the number of records in the current chapter.</span></span>


> [!NOTE]
> <P><span data-ttu-id="66bb6-119">[!NOTA] Para utilizar <STRONG>FetchProgress</STRONG> con Microsoft Visual Basic 6.0, se requiere Visual Basic 6.0 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="66bb6-119">To use <STRONG>FetchProgress</STRONG> with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span></P>


