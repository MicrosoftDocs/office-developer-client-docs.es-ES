---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: 'Libera el objeto de sesión MAPI devuelto por IOlkAccountHelper:: GetMapiSession.'
ms.openlocfilehash: c481cee1ecb8c2bd3997cdee8ae86c9c3b5a712e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418634"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="89f44-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="89f44-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="89f44-104">Libera el objeto de sesión MAPI devuelto por- [IOlkAccountHelper:: GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="89f44-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="89f44-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="89f44-105">Quick info</span></span>

<span data-ttu-id="89f44-106">Consulte [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="89f44-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="89f44-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="89f44-107">Return values</span></span>

|<span data-ttu-id="89f44-108">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="89f44-108">**HRESULT**</span></span>|<span data-ttu-id="89f44-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="89f44-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89f44-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="89f44-110">S_OK</span></span>  <br/> |<span data-ttu-id="89f44-111">Si la implementación de **IOlkAccountHelper** crea su propia sesión MAPI que se devuelve en **IOlkAccountHelper:: GetMapiSession**, debe liberar la sesión aquí y devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="89f44-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="89f44-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="89f44-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="89f44-113">Si la implementación de **IOlkAccountHelper** no crea su propia sesión MAPI, debe devolver sólo E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="89f44-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="89f44-114">En este caso, es el único valor devuelto admitido.</span><span class="sxs-lookup"><span data-stu-id="89f44-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89f44-115">Ver también</span><span class="sxs-lookup"><span data-stu-id="89f44-115">See also</span></span>

- [<span data-ttu-id="89f44-116">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="89f44-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="89f44-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="89f44-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

