---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816838"
---
# <a name="followupstatus"></a><span data-ttu-id="f9e94-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="f9e94-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="f9e94-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9e94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9e94-105">Especifica los diferentes Estados de seguimiento para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f9e94-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f9e94-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f9e94-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="f9e94-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9e94-107">Members</span></span>

 <span data-ttu-id="f9e94-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="f9e94-108">_flwupNone_</span></span>
  
> <span data-ttu-id="f9e94-109">No se ha especificado ningún seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f9e94-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="f9e94-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="f9e94-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="f9e94-111">El mensaje está completado.</span><span class="sxs-lookup"><span data-stu-id="f9e94-111">The message is complete.</span></span>
    
 <span data-ttu-id="f9e94-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="f9e94-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="f9e94-113">El mensaje está marcado para su seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f9e94-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="f9e94-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="f9e94-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="f9e94-115">El número de diferentes estados compatibles para su seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f9e94-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f9e94-116">Ver también</span><span class="sxs-lookup"><span data-stu-id="f9e94-116">See also</span></span>



[<span data-ttu-id="f9e94-117">Propiedad canónico PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="f9e94-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

