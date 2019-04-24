---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.
ms.openlocfilehash: 2511a94678f9ef8f2cb6be868db4f718d92ecb6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317664"
---
# <a name="fbuser"></a><span data-ttu-id="36b75-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="36b75-103">FBUser</span></span>

<span data-ttu-id="36b75-104">Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.</span><span class="sxs-lookup"><span data-stu-id="36b75-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="36b75-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="36b75-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="36b75-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="36b75-106">Members</span></span>

<span data-ttu-id="36b75-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="36b75-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="36b75-108">La longitud del identificador de entrada del usuario de correo, tal como se representa en la interfaz [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) .</span><span class="sxs-lookup"><span data-stu-id="36b75-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="36b75-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="36b75-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="36b75-110">IDENTIFICADOR de entrada del usuario de correo, tal como se representa en la interfaz **IMailUser** .</span><span class="sxs-lookup"><span data-stu-id="36b75-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="36b75-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="36b75-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="36b75-112">Este parámetro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="36b75-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="36b75-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="36b75-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="36b75-114">Este parámetro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="36b75-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36b75-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="36b75-115">See also</span></span>

- [<span data-ttu-id="36b75-116">Acerca de la API de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="36b75-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="36b75-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="36b75-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

