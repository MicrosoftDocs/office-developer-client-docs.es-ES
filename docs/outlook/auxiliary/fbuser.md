---
title: FBUser
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal649b5400-8dc5-cc5c-3455-f462e2d31689
ms.assetid: ''
description: Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.
ms.openlocfilehash: edfc9980445fcc2e111045650667d93bffa94153
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565140"
---
# <a name="fbuser"></a><span data-ttu-id="42b8f-103">FBUser</span><span class="sxs-lookup"><span data-stu-id="42b8f-103">FBUser</span></span>

<span data-ttu-id="42b8f-104">Identifica a un usuario que puede o no tener datos de disponibilidad disponibles.</span><span class="sxs-lookup"><span data-stu-id="42b8f-104">Identifies a user who may or may not have free/busy data available.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="42b8f-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="42b8f-105">Quick info</span></span>

```cpp
typedef struct tagFBUser 
{ 
   ULONG m_cbEid; 
   LPENTRYID m_lpEid; 
   ULONG m_ulReserved; 
   LPWSTR m_pwszReserved; 
} FBUser;

```

## <a name="members"></a><span data-ttu-id="42b8f-106">Members</span><span class="sxs-lookup"><span data-stu-id="42b8f-106">Members</span></span>

<span data-ttu-id="42b8f-107">_m_cbEid_</span><span class="sxs-lookup"><span data-stu-id="42b8f-107">_m_cbEid_</span></span>
  
> <span data-ttu-id="42b8f-108">La longitud del identificador de entrada de usuario de correo, tal como está representado por la interfaz [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) .</span><span class="sxs-lookup"><span data-stu-id="42b8f-108">The length of the entry ID of the mail user as represented by the [IMailUser](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/wab/-wab-imailuser-deleteprops) interface.</span></span> 
    
<span data-ttu-id="42b8f-109">_m_lpEid_</span><span class="sxs-lookup"><span data-stu-id="42b8f-109">_m_lpEid_</span></span>
  
> <span data-ttu-id="42b8f-110">El identificador de entrada del usuario de correo, tal como está representado por la interfaz **IMailUser** .</span><span class="sxs-lookup"><span data-stu-id="42b8f-110">The entry ID of the mail user as represented by the **IMailUser** interface.</span></span> 
    
<span data-ttu-id="42b8f-111">_m_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="42b8f-111">_m_ulReserved_</span></span>
  
> <span data-ttu-id="42b8f-112">Este parámetro está reservado para uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="42b8f-112">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="42b8f-113">_m_pwszReserved_</span><span class="sxs-lookup"><span data-stu-id="42b8f-113">_m_pwszReserved_</span></span>
  
> <span data-ttu-id="42b8f-114">Este parámetro está reservado para uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="42b8f-114">This parameter is reserved for Outlook internal use and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42b8f-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="42b8f-115">See also</span></span>

- [<span data-ttu-id="42b8f-116">Información sobre la API de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="42b8f-116">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="42b8f-117">IFreeBusySupport</span><span class="sxs-lookup"><span data-stu-id="42b8f-117">IFreeBusySupport</span></span>](ifreebusysupport.md)

