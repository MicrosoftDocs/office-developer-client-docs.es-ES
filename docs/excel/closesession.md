---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422540"
---
# <a name="closesession"></a><span data-ttu-id="9c0b5-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="9c0b5-103">CloseSession</span></span>

<span data-ttu-id="9c0b5-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9c0b5-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9c0b5-105">Finaliza una sesión con un clúster.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="9c0b5-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="9c0b5-106">Parameters</span></span>

<span data-ttu-id="9c0b5-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="9c0b5-107">_SessionId_</span></span>
  
> <span data-ttu-id="9c0b5-108">El identificador de la sesión que se cerrará.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-108">The ID of the session to close.</span></span> <span data-ttu-id="9c0b5-109">Este valor debe coincidir con el valor devuelto por [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="9c0b5-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c0b5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c0b5-110">Return value</span></span>

<span data-ttu-id="9c0b5-111">**xlHpcRetSuccess** si la sesión se cerró; **xlHpcRetInvalidSessionId** si el  _argumento SessionId_ no es válido; **xlHpcRetCallFailed en** otros errores.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c0b5-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c0b5-112">See also</span></span>

- [<span data-ttu-id="9c0b5-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="9c0b5-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="9c0b5-114">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="9c0b5-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

