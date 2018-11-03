---
title: onError (evento, RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c67e277c35e3cf6c75226dc138aa4b288843e6bf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930864"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="101e9-102">onError (evento, RDS)</span><span class="sxs-lookup"><span data-stu-id="101e9-102">onError event (RDS)</span></span>


<span data-ttu-id="101e9-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="101e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="101e9-104">El evento **onError** recibe una llamada siempre que se produce un error durante una operación.</span><span class="sxs-lookup"><span data-stu-id="101e9-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="101e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="101e9-105">Syntax</span></span>

<span data-ttu-id="101e9-106">onError*SCode*, *Descripción*, *origen*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="101e9-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="101e9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="101e9-107">Parameters</span></span>

  - <span data-ttu-id="101e9-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="101e9-108">*SCode*</span></span>

  - <span data-ttu-id="101e9-109">Un entero que indica el código de estado del error.</span><span class="sxs-lookup"><span data-stu-id="101e9-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="101e9-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="101e9-110">*Description*</span></span>

  - <span data-ttu-id="101e9-111">Un objeto **String** que indica una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="101e9-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="101e9-112">*Origen*</span><span class="sxs-lookup"><span data-stu-id="101e9-112">*Source*</span></span>

  - <span data-ttu-id="101e9-113">Un objeto **String** que indica la consulta o el comando que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="101e9-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="101e9-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="101e9-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="101e9-115">Una variable de tipo **Boolean** que, si se establece en **True**, evita que se muestre el error en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="101e9-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

