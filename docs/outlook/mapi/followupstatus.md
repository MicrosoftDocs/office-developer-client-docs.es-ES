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
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418333"
---
# <a name="followupstatus"></a><span data-ttu-id="7f083-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="7f083-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="7f083-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f083-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f083-105">Especifica los diferentes estados de seguimiento de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7f083-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7f083-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7f083-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="7f083-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f083-107">Members</span></span>

 <span data-ttu-id="7f083-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="7f083-108">_flwupNone_</span></span>
  
> <span data-ttu-id="7f083-109">No se ha especificado ningún seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7f083-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="7f083-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="7f083-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="7f083-111">El mensaje se ha completado.</span><span class="sxs-lookup"><span data-stu-id="7f083-111">The message is complete.</span></span>
    
 <span data-ttu-id="7f083-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="7f083-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="7f083-113">El mensaje se marca para su seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7f083-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="7f083-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="7f083-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="7f083-115">Número de estados diferentes admitidos para el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7f083-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f083-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7f083-116">See also</span></span>



[<span data-ttu-id="7f083-117">Propiedad canónica PidTagFlagStatus</span><span class="sxs-lookup"><span data-stu-id="7f083-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

