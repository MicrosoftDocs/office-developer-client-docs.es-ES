---
title: onError (evento, RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cbeece67ffa19666f6209a38159c9a2c6a44ea
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889948"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="8fede-102">onError (evento, RDS)</span><span class="sxs-lookup"><span data-stu-id="8fede-102">onError Event (RDS)</span></span>


<span data-ttu-id="8fede-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8fede-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8fede-104">El evento **onError** recibe una llamada siempre que se produce un error durante una operación.</span><span class="sxs-lookup"><span data-stu-id="8fede-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fede-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fede-105">Syntax</span></span>

<span data-ttu-id="8fede-106">onError*SCode*, *Descripción*, *origen*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="8fede-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="8fede-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fede-107">Parameters</span></span>

  - <span data-ttu-id="8fede-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="8fede-108">*SCode*</span></span>

  - <span data-ttu-id="8fede-109">Un entero que indica el código de estado del error.</span><span class="sxs-lookup"><span data-stu-id="8fede-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="8fede-110">*Description*</span><span class="sxs-lookup"><span data-stu-id="8fede-110">*Description*</span></span>

  - <span data-ttu-id="8fede-111">Un objeto **String** que indica una descripción del error.</span><span class="sxs-lookup"><span data-stu-id="8fede-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="8fede-112">*Origen*</span><span class="sxs-lookup"><span data-stu-id="8fede-112">*Source*</span></span>

  - <span data-ttu-id="8fede-113">Un objeto **String** que indica la consulta o el comando que produjo el error.</span><span class="sxs-lookup"><span data-stu-id="8fede-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="8fede-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="8fede-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="8fede-115">Una variable de tipo **Boolean** que, si se establece en **True**, evita que se muestre el error en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8fede-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

