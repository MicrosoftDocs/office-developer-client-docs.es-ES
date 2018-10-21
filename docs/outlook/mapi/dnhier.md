---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389088"
---
# <a name="dnhier"></a><span data-ttu-id="7d3a9-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="7d3a9-103">DNHIER</span></span>

<span data-ttu-id="7d3a9-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d3a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d3a9-105">Información para descargar una jerarquía del servidor durante el [estado de descarga de jerarquía](download-hierarchy-state.md), que forma parte de la sincronización de jerarquía completa.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="7d3a9-106">Este proceso de descarga usa la sincronización de cambio incremental (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="7d3a9-107">Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d3a9-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7d3a9-108">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7d3a9-108">Quick Info</span></span>

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="7d3a9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d3a9-109">Members</span></span>

<span data-ttu-id="7d3a9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d3a9-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="7d3a9-111">[entrada] Indicadores para determinar el comportamiento adecuado durante la descarga.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="7d3a9-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="7d3a9-112">DNH_OK</span></span>
    
   - <span data-ttu-id="7d3a9-113">[entrada] La descarga se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-113">[in] Download was successful.</span></span> <span data-ttu-id="7d3a9-114">El cliente lo establece después de descargar la información del servidor.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="7d3a9-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="7d3a9-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="7d3a9-116">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7d3a9-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="7d3a9-117">_pxihc_</span></span>
  
>  <span data-ttu-id="7d3a9-118">[salida] Puntero a la interfaz de contenido **IExchangeImportHierarchyChanges** que admite la descarga de los cambios de jerarquía incremental.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="7d3a9-119">Para más información sobre **IExchangeImportHierarchyChanges**, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d3a9-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="7d3a9-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="7d3a9-120">_cEntNew_</span></span>
  
> <span data-ttu-id="7d3a9-121">[salida] Número de carpetas añadidas al almacén local.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="7d3a9-122">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="7d3a9-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="7d3a9-123">_cEntMod_</span></span>
  
> <span data-ttu-id="7d3a9-124">[salida] Número de carpetas que se modificarán en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="7d3a9-125">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="7d3a9-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="7d3a9-126">_cEntDel_</span></span>
  
> <span data-ttu-id="7d3a9-127">[salida] Número de carpetas que se eliminarán en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="7d3a9-128">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="7d3a9-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d3a9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d3a9-129">See also</span></span>

- [<span data-ttu-id="7d3a9-130">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="7d3a9-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="7d3a9-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7d3a9-131">MAPI Constants</span></span>](mapi-constants.md)

