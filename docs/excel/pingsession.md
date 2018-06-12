---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815705"
---
# <a name="pingsession"></a><span data-ttu-id="8dad8-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="8dad8-103">PingSession</span></span>

<span data-ttu-id="8dad8-104">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8dad8-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8dad8-105">Comprueba si una sesión es válida.</span><span class="sxs-lookup"><span data-stu-id="8dad8-105">Checks whether a session is valid.</span></span> <span data-ttu-id="8dad8-106">Normalmente, se llama a esta función cuando Excel necesita para determinar si un identificador de sesión devueltos anteriormente todavía está activo y se puede usar.</span><span class="sxs-lookup"><span data-stu-id="8dad8-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="8dad8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8dad8-107">Parameters</span></span>

<span data-ttu-id="8dad8-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="8dad8-108">_SessionID_</span></span>
  
> <span data-ttu-id="8dad8-109">El identificador de la sesión para hacer ping.</span><span class="sxs-lookup"><span data-stu-id="8dad8-109">The ID of the session to ping.</span></span> <span data-ttu-id="8dad8-110">Este valor debe coincidir con un identificador devuelto por una llamada anterior a [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="8dad8-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8dad8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8dad8-111">Return value</span></span>

<span data-ttu-id="8dad8-112">**xlHpcRetSuccess** si el argumento de _SessionId_ es válido; en caso contrario, **xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="8dad8-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8dad8-113">Ver también</span><span class="sxs-lookup"><span data-stu-id="8dad8-113">See also</span></span>

- [<span data-ttu-id="8dad8-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="8dad8-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="8dad8-115">Funciones de conector de clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="8dad8-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

