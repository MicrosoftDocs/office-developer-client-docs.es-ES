---
title: UPTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 39d9ad3b-ff4b-8378-a3ac-d5621c7ef7f1
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 70d23bebfda10339ffb05f573c8c309a44f09d7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820968"
---
# <a name="uptbl"></a><span data-ttu-id="e045b-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="e045b-103">UPTBL</span></span>

<span data-ttu-id="e045b-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e045b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e045b-105">Información para cargar el contenido de una carpeta durante la [carga de estado de la tabla](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="e045b-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e045b-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="e045b-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="e045b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e045b-107">Members</span></span>

<span data-ttu-id="e045b-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e045b-108">_ulFlags_</span></span>
  
> <span data-ttu-id="e045b-109">[entrada] Marcas para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="e045b-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="e045b-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="e045b-110">UPT_OK</span></span>
    
    - <span data-ttu-id="e045b-111">[entrada] Carga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="e045b-111">[in] Upload was successful.</span></span> <span data-ttu-id="e045b-112">El cliente establece esto después de cargar el contenido de la carpeta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="e045b-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="e045b-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="e045b-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="e045b-114">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="e045b-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e045b-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="e045b-115">_pszName_</span></span>
  
> <span data-ttu-id="e045b-116">[out] Nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e045b-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="e045b-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="e045b-117">_feid_</span></span>
  
> <span data-ttu-id="e045b-118">[out] Identificador de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e045b-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="e045b-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="e045b-119">_uintReserved_</span></span>
  
> <span data-ttu-id="e045b-120">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="e045b-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e045b-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="e045b-121">_rgte_</span></span>
  
> <span data-ttu-id="e045b-122">[out] Estructura para contener la siguiente información para elementos normales (o no ocultos) y elementos asociados (u ocultos) en la carpeta: _rgte [0]_ es para los elementos normales y _rgte [1]_ es para los elementos asociados.</span><span class="sxs-lookup"><span data-stu-id="e045b-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="e045b-123">el número de elementos nuevos o modificados</span><span class="sxs-lookup"><span data-stu-id="e045b-123">the number of new or modified items</span></span>
   - <span data-ttu-id="e045b-124">el número de elementos leídos</span><span class="sxs-lookup"><span data-stu-id="e045b-124">the number of read items</span></span> 
   - <span data-ttu-id="e045b-125">el número de elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="e045b-125">the number of deleted items</span></span>
    
 <span data-ttu-id="e045b-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="e045b-126">_iEnt_</span></span>
  
> <span data-ttu-id="e045b-127">[out] Índice que se va a realizar un seguimiento de cargar el número de cambios especificado por _ciento_.</span><span class="sxs-lookup"><span data-stu-id="e045b-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="e045b-128">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="e045b-128">_cEnt_</span></span>
  
> <span data-ttu-id="e045b-129">[out] Número de los cambios realizados en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e045b-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="e045b-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="e045b-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="e045b-131">[out] Cadena de estructuras [UPMOV](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="e045b-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="e045b-132">_Conserva_</span><span class="sxs-lookup"><span data-stu-id="e045b-132">_pReserved_</span></span>
  
> <span data-ttu-id="e045b-133">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="e045b-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e045b-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="e045b-134">See also</span></span>

- [<span data-ttu-id="e045b-135">Acerca de la API de replicación</span><span class="sxs-lookup"><span data-stu-id="e045b-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="e045b-136">Acerca de la máquina de estado de replicación</span><span class="sxs-lookup"><span data-stu-id="e045b-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e045b-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e045b-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="e045b-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="e045b-138">UPTBLE</span></span>](uptble.md)

