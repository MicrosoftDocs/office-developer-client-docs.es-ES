---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568521"
---
# <a name="followupstatus"></a><span data-ttu-id="2c0b8-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="2c0b8-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="2c0b8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c0b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c0b8-105">Especifica los diferentes Estados de seguimiento para un mensaje.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2c0b8-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="2c0b8-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="2c0b8-107">Members</span><span class="sxs-lookup"><span data-stu-id="2c0b8-107">Members</span></span>

 <span data-ttu-id="2c0b8-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="2c0b8-108">_flwupNone_</span></span>
  
> <span data-ttu-id="2c0b8-109">No se ha especificado ningún seguimiento.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="2c0b8-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="2c0b8-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="2c0b8-111">El mensaje está completado.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-111">The message is complete.</span></span>
    
 <span data-ttu-id="2c0b8-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="2c0b8-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="2c0b8-113">El mensaje está marcado para su seguimiento.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="2c0b8-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="2c0b8-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="2c0b8-115">El número de diferentes estados compatibles para su seguimiento.</span><span class="sxs-lookup"><span data-stu-id="2c0b8-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c0b8-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2c0b8-116">See also</span></span>



[<span data-ttu-id="2c0b8-117">Propiedad canónica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="2c0b8-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

