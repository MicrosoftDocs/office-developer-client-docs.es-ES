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
ms.openlocfilehash: b401f54df020fb6553cbdcc5b85206ee422a8429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338860"
---
# <a name="uptbl"></a><span data-ttu-id="61776-103">UPTBL</span><span class="sxs-lookup"><span data-stu-id="61776-103">UPTBL</span></span>

<span data-ttu-id="61776-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61776-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61776-105">Información para cargar el contenido de una carpeta durante el estado de [carga](upload-table-state.md)de la tabla.</span><span class="sxs-lookup"><span data-stu-id="61776-105">Information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="61776-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="61776-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="61776-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="61776-107">Members</span></span>

<span data-ttu-id="61776-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61776-108">_ulFlags_</span></span>
  
> <span data-ttu-id="61776-109">a Marcas para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="61776-109">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="61776-110">UPT_OK</span><span class="sxs-lookup"><span data-stu-id="61776-110">UPT_OK</span></span>
    
    - <span data-ttu-id="61776-111">a La carga se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="61776-111">[in] Upload was successful.</span></span> <span data-ttu-id="61776-112">El cliente lo establece después de cargar el contenido de la carpeta en el servidor.</span><span class="sxs-lookup"><span data-stu-id="61776-112">The client sets this after uploading the folder contents to the server.</span></span>
    
<span data-ttu-id="61776-113">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="61776-113">_pstmReserved_</span></span>
  
> <span data-ttu-id="61776-114">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="61776-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="61776-115">_pszName_</span><span class="sxs-lookup"><span data-stu-id="61776-115">_pszName_</span></span>
  
> <span data-ttu-id="61776-116">[salida] Nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="61776-116">[out] Name of the folder.</span></span>
    
<span data-ttu-id="61776-117">_feid_</span><span class="sxs-lookup"><span data-stu-id="61776-117">_feid_</span></span>
  
> <span data-ttu-id="61776-118">[salida] Id. de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="61776-118">[out] Entry ID of the folder.</span></span>
    
<span data-ttu-id="61776-119">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="61776-119">_uintReserved_</span></span>
  
> <span data-ttu-id="61776-120">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="61776-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="61776-121">_rgte_</span><span class="sxs-lookup"><span data-stu-id="61776-121">_rgte_</span></span>
  
> <span data-ttu-id="61776-122">contempla Estructura para contener la siguiente información para elementos normales (o no ocultos) y elementos asociados (u ocultos) en la carpeta: _rgte [0]_ es para los elementos normales y _rgte [1]_ es para los elementos asociados.</span><span class="sxs-lookup"><span data-stu-id="61776-122">[out] Structure to hold the following information for normal (or non-hidden) items and associated (or hidden) items in the folder:  _rgte[0]_ is for normal items, and  _rgte[1]_ is for associated items.</span></span> 
    
   - <span data-ttu-id="61776-123">el número de elementos nuevos o modificados</span><span class="sxs-lookup"><span data-stu-id="61776-123">the number of new or modified items</span></span>
   - <span data-ttu-id="61776-124">el número de elementos leídos</span><span class="sxs-lookup"><span data-stu-id="61776-124">the number of read items</span></span> 
   - <span data-ttu-id="61776-125">número de elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="61776-125">the number of deleted items</span></span>
    
 <span data-ttu-id="61776-126">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="61776-126">_iEnt_</span></span>
  
> <span data-ttu-id="61776-127">contempla Índice para realizar un seguimiento de la carga del número de cambios especificado en el _céntimo_.</span><span class="sxs-lookup"><span data-stu-id="61776-127">[out] Index to track uploading the number of changes specified by  _cEnt_.</span></span>
    
<span data-ttu-id="61776-128">_Ciento_</span><span class="sxs-lookup"><span data-stu-id="61776-128">_cEnt_</span></span>
  
> <span data-ttu-id="61776-129">contempla Número de cambios en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="61776-129">[out] Number of changes to the folder.</span></span>
    
<span data-ttu-id="61776-130">_pupmovHead_</span><span class="sxs-lookup"><span data-stu-id="61776-130">_pupmovHead_</span></span>
  
> <span data-ttu-id="61776-131">contempla Cadena de estructuras [UPMOV](upmov.md) .</span><span class="sxs-lookup"><span data-stu-id="61776-131">[out] Chain of [UPMOV](upmov.md) structures.</span></span> 
    
<span data-ttu-id="61776-132">_Preserva_</span><span class="sxs-lookup"><span data-stu-id="61776-132">_pReserved_</span></span>
  
> <span data-ttu-id="61776-133">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="61776-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61776-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="61776-134">See also</span></span>

- [<span data-ttu-id="61776-135">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="61776-135">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="61776-136">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="61776-136">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="61776-137">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="61776-137">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="61776-138">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="61776-138">UPTBLE</span></span>](uptble.md)

