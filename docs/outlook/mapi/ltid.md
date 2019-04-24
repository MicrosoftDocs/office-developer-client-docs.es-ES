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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357417"
---
# <a name="ltid"></a><span data-ttu-id="0ac88-103">LTID</span><span class="sxs-lookup"><span data-stu-id="0ac88-103">LTID</span></span>

  
  
<span data-ttu-id="0ac88-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ac88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ac88-105">IDENTIFICADOR de término largo genérico de un objeto en un almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="0ac88-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0ac88-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="0ac88-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="0ac88-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ac88-107">Members</span></span>

 <span data-ttu-id="0ac88-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="0ac88-108">_guid_</span></span>
  
- <span data-ttu-id="0ac88-109">contempla GUID del servidor que creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="0ac88-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="0ac88-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="0ac88-110">_globcnt_</span></span>
  
- <span data-ttu-id="0ac88-111">contempla Un número único de 6 bytes que identifica el objeto en el almacén de Outlook.</span><span class="sxs-lookup"><span data-stu-id="0ac88-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="0ac88-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="0ac88-112">_wLevel_</span></span>
  
- <span data-ttu-id="0ac88-113">contempla El nivel de jerarquía del identificador de entrada de una carpeta pública favorita de Exchange.</span><span class="sxs-lookup"><span data-stu-id="0ac88-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ac88-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ac88-114">See also</span></span>



[<span data-ttu-id="0ac88-115">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="0ac88-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="0ac88-116">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="0ac88-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="0ac88-117">FEID</span><span class="sxs-lookup"><span data-stu-id="0ac88-117">FEID</span></span>](feid.md)

