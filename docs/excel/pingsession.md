---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301620"
---
# <a name="pingsession"></a><span data-ttu-id="3ca30-103">PingSession</span><span class="sxs-lookup"><span data-stu-id="3ca30-103">PingSession</span></span>

<span data-ttu-id="3ca30-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ca30-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3ca30-105">Comprueba si una sesión es válida.</span><span class="sxs-lookup"><span data-stu-id="3ca30-105">Checks whether a session is valid.</span></span> <span data-ttu-id="3ca30-106">Normalmente, se llama a esta función cuando Excel necesita determinar si un identificador de sesión devuelto anteriormente todavía está activo y se puede usar.</span><span class="sxs-lookup"><span data-stu-id="3ca30-106">This function is typically called when Excel needs to determine if a previously returned session ID is still active and can be used.</span></span>
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="3ca30-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="3ca30-107">Parameters</span></span>

<span data-ttu-id="3ca30-108">_SessionID_</span><span class="sxs-lookup"><span data-stu-id="3ca30-108">_SessionID_</span></span>
  
> <span data-ttu-id="3ca30-109">IDENTIFICADOR de la sesión a la que se va a hacer ping.</span><span class="sxs-lookup"><span data-stu-id="3ca30-109">The ID of the session to ping.</span></span> <span data-ttu-id="3ca30-110">Este valor debe coincidir con un identificador devuelto por una llamada anterior a [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="3ca30-110">This value must match an ID returned by a previous call to [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ca30-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ca30-111">Return value</span></span>

<span data-ttu-id="3ca30-112">**xlHpcRetSuccess** si el argumento _SessionID_ es válido; de lo contrario **xlHpcRetInvalidSessionId**.</span><span class="sxs-lookup"><span data-stu-id="3ca30-112">**xlHpcRetSuccess** if the  _SessionId_ argument is valid; otherwise **xlHpcRetInvalidSessionId**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ca30-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ca30-113">See also</span></span>

- [<span data-ttu-id="3ca30-114">OpenSession</span><span class="sxs-lookup"><span data-stu-id="3ca30-114">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="3ca30-115">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="3ca30-115">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

