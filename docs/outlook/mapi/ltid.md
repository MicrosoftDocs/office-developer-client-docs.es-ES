---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818040"
---
# <a name="ltid"></a><span data-ttu-id="f7c3f-103">LTID</span><span class="sxs-lookup"><span data-stu-id="f7c3f-103">LTID</span></span>

  
  
<span data-ttu-id="f7c3f-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f7c3f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f7c3f-105">Largo términos identificador genérico de un objeto en un almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="f7c3f-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f7c3f-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f7c3f-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="f7c3f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f7c3f-107">Members</span></span>

 <span data-ttu-id="f7c3f-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="f7c3f-108">_guid_</span></span>
  
- <span data-ttu-id="f7c3f-109">[out] El GUID del servidor que creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="f7c3f-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="f7c3f-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="f7c3f-110">_globcnt_</span></span>
  
- <span data-ttu-id="f7c3f-111">[out] Número único de 6 bytes que identifica el objeto en el almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="f7c3f-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="f7c3f-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="f7c3f-112">_wLevel_</span></span>
  
- <span data-ttu-id="f7c3f-113">[out] El nivel de la jerarquía del identificador de entrada para una carpeta pública Favoritos de Exchange.</span><span class="sxs-lookup"><span data-stu-id="f7c3f-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7c3f-114">Ver también</span><span class="sxs-lookup"><span data-stu-id="f7c3f-114">See also</span></span>



[<span data-ttu-id="f7c3f-115">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="f7c3f-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="f7c3f-116">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="f7c3f-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="f7c3f-117">FEID</span><span class="sxs-lookup"><span data-stu-id="f7c3f-117">FEID</span></span>](feid.md)

