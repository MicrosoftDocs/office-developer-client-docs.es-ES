---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bdfabdf02fc0fa6222418bd0fb87e9b6c17d936a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580442"
---
# <a name="uptbl"></a><span data-ttu-id="9f689-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="9f689-103">UPTBL</span></span>

<span data-ttu-id="9f689-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f689-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f689-105">Información para cargar el contenido de una carpeta durante la [carga de estado de la tabla](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="9f689-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9f689-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="9f689-106">Quick info</span></span>

```cpp
struct UPTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    LPSTR pszName; 
    FEID feid; 
    UINT uintReserved; 
    UPTBLE rgte[2]; 
    UINT iEnt; 
    UINT cEnt; 
    PUPMOV pupmovHead; 
    void* pReserved; 
};
```

## <a name="members"></a><span data-ttu-id="9f689-107">Members</span><span class="sxs-lookup"><span data-stu-id="9f689-107">Members</span></span>

<span data-ttu-id="9f689-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9f689-108">_ulFlags_</span></span>
  
> <span data-ttu-id="9f689-109">[entrada] Marcas para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="9f689-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="9f689-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="9f689-110">UPT_OK</span></span>
    
    - <span data-ttu-id="9f689-111">[entrada] Carga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="9f689-111">[in] Upload was successful.</span></span> <span data-ttu-id="9f689-112">El cliente establece esto después de cargar el contenido de la carpeta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="9f689-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="9f689-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="9f689-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="9f689-114">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="9f689-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="9f689-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="9f689-115">_pszName_</span></span>
  
> <span data-ttu-id="9f689-116">[out] Nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9f689-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="9f689-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="9f689-117">_feid_</span></span>
  
> <span data-ttu-id="9f689-118">[out] Identificador de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9f689-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="9f689-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="9f689-119">_uintReserved_</span></span>
  
> <span data-ttu-id="9f689-120">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="9f689-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="9f689-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="9f689-121">_rgte_</span></span>
  
> <span data-ttu-id="9f689-122">[out] Estructura para contener la siguiente información para elementos normales (o no ocultos) y elementos asociados (u ocultos) en la carpeta: _rgte [0]_ es para los elementos normales y _rgte [1]_ es para los elementos asociados.</span><span class="sxs-lookup"><span data-stu-id="9f689-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="9f689-123">el número de elementos nuevos o modificados</span><span class="sxs-lookup"><span data-stu-id="9f689-123">the number of new or modified items</span></span>
   - <span data-ttu-id="9f689-124">el número de elementos leídos</span><span class="sxs-lookup"><span data-stu-id="9f689-124">the number of read items</span></span> 
   - <span data-ttu-id="9f689-125">el número de elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="9f689-125">the number of deleted items</span></span>
    
 <span data-ttu-id="9f689-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="9f689-126">_iEnt_</span></span>
  
> <span data-ttu-id="9f689-127">[out] Índice que se va a realizar un seguimiento de cargar el número de cambios especificado por _ciento_.</span><span class="sxs-lookup"><span data-stu-id="9f689-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="9f689-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="9f689-128">_cEnt_</span></span>
  
> <span data-ttu-id="9f689-129">[out] Número de los cambios realizados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="9f689-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="9f689-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="9f689-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="9f689-131">[out] Cadena de estructuras [UPMOV](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="9f689-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="9f689-132">_Conserva_</span><span class="sxs-lookup"><span data-stu-id="9f689-132">_pReserved_</span></span>
  
> <span data-ttu-id="9f689-133">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="9f689-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f689-134">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="9f689-134">See also</span></span>

- [<span data-ttu-id="9f689-135">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="9f689-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="9f689-136">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="9f689-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="9f689-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9f689-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="9f689-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="9f689-138">UPTBLE</span></span>](uptble.md)

