---
title: evento onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288479"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="98b6d-102">evento onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="98b6d-102">onError event (RDS)</span></span>

<span data-ttu-id="98b6d-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98b6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98b6d-104">El evento **onError** recibe una llamada siempre que se produce un error durante una operación.</span><span class="sxs-lookup"><span data-stu-id="98b6d-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b6d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98b6d-105">Syntax</span></span>

<span data-ttu-id="98b6d-106">onError *SCode*, *Description*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="98b6d-106">onError *SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="98b6d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98b6d-107">Parameters</span></span>

|<span data-ttu-id="98b6d-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="98b6d-108">Parameter</span></span>|<span data-ttu-id="98b6d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="98b6d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="98b6d-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="98b6d-110">*SCode*</span></span> |<span data-ttu-id="98b6d-111">Un entero que indica el código de estado del error.</span><span class="sxs-lookup"><span data-stu-id="98b6d-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="98b6d-112">*Description*</span><span class="sxs-lookup"><span data-stu-id="98b6d-112">*Description*</span></span> |<span data-ttu-id="98b6d-113">Un objeto **String** que indica una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="98b6d-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="98b6d-114">*Origen*</span><span class="sxs-lookup"><span data-stu-id="98b6d-114">*Source*</span></span> |<span data-ttu-id="98b6d-115">Un objeto **String** que indica la consulta o el comando que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="98b6d-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="98b6d-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="98b6d-116">*CancelDisplay*</span></span> |<span data-ttu-id="98b6d-117">Una variable de tipo **Boolean** que, si se establece en **True**, evita que se muestre el error en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="98b6d-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

