---
title: onError (evento, RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486451"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="dedfb-102">onError (evento, RDS)</span><span class="sxs-lookup"><span data-stu-id="dedfb-102">onError Event (RDS)</span></span>


<span data-ttu-id="dedfb-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dedfb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dedfb-104">El evento **onError** recibe una llamada siempre que se produce un error durante una operación.</span><span class="sxs-lookup"><span data-stu-id="dedfb-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dedfb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dedfb-105">Syntax</span></span>

<span data-ttu-id="dedfb-106">onError*SCode*, *Descripción*, *origen*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="dedfb-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="dedfb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dedfb-107">Parameters</span></span>

  - <span data-ttu-id="dedfb-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="dedfb-108">*SCode*</span></span>

  - <span data-ttu-id="dedfb-109">Un entero que indica el código de estado del error.</span><span class="sxs-lookup"><span data-stu-id="dedfb-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="dedfb-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="dedfb-110">*Description*</span></span>

  - <span data-ttu-id="dedfb-111">Un objeto **String** que indica una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="dedfb-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="dedfb-112">*Origen*</span><span class="sxs-lookup"><span data-stu-id="dedfb-112">*Source*</span></span>

  - <span data-ttu-id="dedfb-113">Un objeto **String** que indica la consulta o el comando que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="dedfb-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="dedfb-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="dedfb-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="dedfb-115">Una variable de tipo **Boolean** que, si se establece en **True**, evita que se muestre el error en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="dedfb-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

