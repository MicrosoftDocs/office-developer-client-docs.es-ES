---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815529"
---
# <a name="closesession"></a><span data-ttu-id="438d7-103">CloseSession</span><span class="sxs-lookup"><span data-stu-id="438d7-103">CloseSession</span></span>

<span data-ttu-id="438d7-104">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="438d7-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="438d7-105">Termina una sesión con un clúster.</span><span class="sxs-lookup"><span data-stu-id="438d7-105">Ends a session with a cluster.</span></span>
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a><span data-ttu-id="438d7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="438d7-106">Parameters</span></span>

<span data-ttu-id="438d7-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="438d7-107">_SessionId_</span></span>
  
> <span data-ttu-id="438d7-108">El identificador de la sesión para cerrar.</span><span class="sxs-lookup"><span data-stu-id="438d7-108">The ID of the session to close.</span></span> <span data-ttu-id="438d7-109">Este valor debe coincidir con el valor devuelto por [OpenSession](opensession.md).</span><span class="sxs-lookup"><span data-stu-id="438d7-109">This value must match the value returned by [OpenSession](opensession.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="438d7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="438d7-110">Return value</span></span>

<span data-ttu-id="438d7-111">**xlHpcRetSuccess** si ha cerrado la sesión; **xlHpcRetInvalidSessionId** si el argumento de _SessionId_ no es válido; **xlHpcRetCallFailed** en otros errores.</span><span class="sxs-lookup"><span data-stu-id="438d7-111">**xlHpcRetSuccess** if the session closed; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="438d7-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="438d7-112">See also</span></span>

- [<span data-ttu-id="438d7-113">OpenSession</span><span class="sxs-lookup"><span data-stu-id="438d7-113">OpenSession</span></span>](opensession.md)
- [<span data-ttu-id="438d7-114">Funciones de conectores clúster de Excel</span><span class="sxs-lookup"><span data-stu-id="438d7-114">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
