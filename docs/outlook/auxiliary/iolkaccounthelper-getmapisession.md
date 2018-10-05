---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: Se abre una sesión MAPI y mantiene una referencia a la sesión para el Administrador de cuentas.
ms.openlocfilehash: 5886ac1ae1bb8f3b43e09f49e48434d9a73656ce
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392607"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="9cf75-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="9cf75-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="9cf75-104">Se abre una sesión MAPI y mantiene una referencia a la sesión para el Administrador de cuentas.</span><span class="sxs-lookup"><span data-stu-id="9cf75-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9cf75-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9cf75-105">Quick info</span></span>

<span data-ttu-id="9cf75-106">Vea [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="9cf75-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="9cf75-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9cf75-107">Parameters</span></span>

<span data-ttu-id="9cf75-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="9cf75-108">_ppmsess_</span></span>
  
> <span data-ttu-id="9cf75-109">[out] La sesión MAPI actual.</span><span class="sxs-lookup"><span data-stu-id="9cf75-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="9cf75-110">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="9cf75-110">Return values</span></span>

<span data-ttu-id="9cf75-111">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="9cf75-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9cf75-112">Notas</span><span class="sxs-lookup"><span data-stu-id="9cf75-112">Remarks</span></span>

<span data-ttu-id="9cf75-113">Debido a problemas de referencia circular, el Administrador de cuentas de sí mismo no puede mantener la referencia de la sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="9cf75-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9cf75-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cf75-114">See also</span></span>

- [<span data-ttu-id="9cf75-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="9cf75-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="9cf75-116">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9cf75-116">IMAPISession : IUnknown</span></span>](https://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

