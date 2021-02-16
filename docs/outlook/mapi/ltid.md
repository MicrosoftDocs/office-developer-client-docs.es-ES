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
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419439"
---
# <a name="ltid"></a><span data-ttu-id="85e93-103">LTID</span><span class="sxs-lookup"><span data-stu-id="85e93-103">LTID</span></span>

  
  
<span data-ttu-id="85e93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85e93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85e93-105">Identificador genérico a largo plazo de un objeto en un almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="85e93-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="85e93-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="85e93-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="85e93-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="85e93-107">Members</span></span>

 <span data-ttu-id="85e93-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="85e93-108">_guid_</span></span>
  
- <span data-ttu-id="85e93-109">[salida] GUID del servidor que creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="85e93-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="85e93-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="85e93-110">_globcnt_</span></span>
  
- <span data-ttu-id="85e93-111">[salida] Un número único de 6 bytes que identifica el objeto dentro del almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="85e93-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="85e93-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="85e93-112">_wLevel_</span></span>
  
- <span data-ttu-id="85e93-113">[salida] Nivel de jerarquía del identificador de entrada de una carpeta pública favorita de Exchange.</span><span class="sxs-lookup"><span data-stu-id="85e93-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85e93-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85e93-114">See also</span></span>



[<span data-ttu-id="85e93-115">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="85e93-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="85e93-116">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="85e93-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="85e93-117">FEID</span><span class="sxs-lookup"><span data-stu-id="85e93-117">FEID</span></span>](feid.md)

