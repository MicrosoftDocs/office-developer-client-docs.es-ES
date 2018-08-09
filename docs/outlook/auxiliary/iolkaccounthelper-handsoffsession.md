---
title: IOlkAccountHelperHandsOffSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9f71fdef-5df5-0892-b64c-293a2f22f5c3
description: Libera el objeto de sesión MAPI que se ha devuelto por IOlkAccountHelper::GetMapiSession.
ms.openlocfilehash: 71931be73e75e858224d3da2c92071341ac45e72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816212"
---
# <a name="iolkaccounthelperhandsoffsession"></a><span data-ttu-id="17ac8-103">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="17ac8-103">IOlkAccountHelper::HandsOffSession</span></span>

<span data-ttu-id="17ac8-104">Libera el objeto de sesión MAPI que se ha devuelto por - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="17ac8-104">Releases the MAPI session object that was returned by - [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="17ac8-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="17ac8-105">Quick info</span></span>

<span data-ttu-id="17ac8-106">Vea [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="17ac8-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::HandsOffSession( );
```

## <a name="return-values"></a><span data-ttu-id="17ac8-107">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="17ac8-107">Return values</span></span>

|<span data-ttu-id="17ac8-108">**[HRESULT]**</span><span class="sxs-lookup"><span data-stu-id="17ac8-108">**HRESULT**</span></span>|<span data-ttu-id="17ac8-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="17ac8-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="17ac8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="17ac8-110">S_OK</span></span>  <br/> |<span data-ttu-id="17ac8-111">Si su implementación de **IOlkAccountHelper** crea su propia sesión MAPI que se devuelve en **IOlkAccountHelper::GetMapiSession**, debe liberar la sesión aquí y devolver S_OK.</span><span class="sxs-lookup"><span data-stu-id="17ac8-111">If your implementation of **IOlkAccountHelper** creates its own MAPI session that is returned in **IOlkAccountHelper::GetMapiSession**, you must release the session here and return S_OK.</span></span>  <br/> |
|<span data-ttu-id="17ac8-112">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="17ac8-112">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="17ac8-113">Si su implementación de **IOlkAccountHelper** no ha creado su propia sesión MAPI, debe devolver sólo E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="17ac8-113">If your implementation of **IOlkAccountHelper** did not create its own MAPI session, you must return only E_NOTIMPL.</span></span> <span data-ttu-id="17ac8-114">En este caso, esto es el único valor devuelto admitido.</span><span class="sxs-lookup"><span data-stu-id="17ac8-114">In this case, this is the only supported return value.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17ac8-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="17ac8-115">See also</span></span>

- [<span data-ttu-id="17ac8-116">Constantes (API de administración de cuenta)</span><span class="sxs-lookup"><span data-stu-id="17ac8-116">Constants (Account management API)</span></span>](constants-account-management-api.md)  
- [<span data-ttu-id="17ac8-117">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="17ac8-117">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md)

