---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414924"
---
# <a name="uphier"></a><span data-ttu-id="6a867-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="6a867-103">UPHIER</span></span>
 
<span data-ttu-id="6a867-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a867-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a867-105">Información para sincronizar una jerarquía de carpetas durante el [Estado de carga](upload-hierarchy-state.md)de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="6a867-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6a867-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="6a867-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="6a867-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6a867-107">Members</span></span>

<span data-ttu-id="6a867-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a867-108">_ulFlags_</span></span>
  
> <span data-ttu-id="6a867-109">a Marcas para modificar el comportamiento al sincronizar la jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="6a867-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="6a867-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="6a867-110">UPH_OK</span></span>
    
    - <span data-ttu-id="6a867-111">a La carga se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6a867-111">[in] Upload was successful.</span></span> <span data-ttu-id="6a867-112">El cliente lo establece después de cargar correctamente la información en el servidor.</span><span class="sxs-lookup"><span data-stu-id="6a867-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="6a867-113">Una vez que se ve esta marca, Outlook borra la información interna de contabilidad que indicó que era necesario actualizar la jerarquía de carpetas.</span><span class="sxs-lookup"><span data-stu-id="6a867-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="6a867-114">El cliente pasa el HRESULT si la carga no se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6a867-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="6a867-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="6a867-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="6a867-116">contempla Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="6a867-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="6a867-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="6a867-117">_iEnt_</span></span>
  
> <span data-ttu-id="6a867-118">contempla Índice para realizar un seguimiento de la sincronización del número de carpetas especificado en *cEnt* .</span><span class="sxs-lookup"><span data-stu-id="6a867-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="6a867-119">_Ciento_</span><span class="sxs-lookup"><span data-stu-id="6a867-119">_cEnt_</span></span>
  
> <span data-ttu-id="6a867-120">contempla Número de carpetas que no están sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="6a867-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6a867-121">Ver también</span><span class="sxs-lookup"><span data-stu-id="6a867-121">See also</span></span>

- [<span data-ttu-id="6a867-122">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="6a867-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="6a867-123">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="6a867-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="6a867-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="6a867-124">MAPI Constants</span></span>](mapi-constants.md)

