---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569858"
---
# <a name="ltid"></a><span data-ttu-id="315e3-103">LTID</span><span class="sxs-lookup"><span data-stu-id="315e3-103">LTID</span></span>

  
  
<span data-ttu-id="315e3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="315e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="315e3-105">Largo términos identificador genérico de un objeto en un almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="315e3-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="315e3-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="315e3-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="315e3-107">Members</span><span class="sxs-lookup"><span data-stu-id="315e3-107">Members</span></span>

 <span data-ttu-id="315e3-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="315e3-108">_guid_</span></span>
  
- <span data-ttu-id="315e3-109">[out] El GUID del servidor que creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="315e3-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="315e3-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="315e3-110">_globcnt_</span></span>
  
- <span data-ttu-id="315e3-111">[out] Número único de 6 bytes que identifica el objeto en el almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="315e3-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="315e3-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="315e3-112">_wLevel_</span></span>
  
- <span data-ttu-id="315e3-113">[out] El nivel de la jerarquía del identificador de entrada para una carpeta pública Favoritos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="315e3-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="315e3-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="315e3-114">See also</span></span>



[<span data-ttu-id="315e3-115">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="315e3-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="315e3-116">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="315e3-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="315e3-117">FEID</span><span class="sxs-lookup"><span data-stu-id="315e3-117">FEID</span></span>](feid.md)

