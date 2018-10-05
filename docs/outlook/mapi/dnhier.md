---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389088"
---
# <a name="dnhier"></a><span data-ttu-id="8647e-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="8647e-103">DNHIER</span></span>

<span data-ttu-id="8647e-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8647e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8647e-105">Información para la descarga de una jerarquía desde el servidor durante el [estado de la jerarquía de descarga](download-hierarchy-state.md), que forma parte de una sincronización completa de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="8647e-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="8647e-106">Este proceso de descarga utiliza sincronización de cambio Incremental (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="8647e-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="8647e-107">Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8647e-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8647e-108">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8647e-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8647e-109">Members</span><span class="sxs-lookup"><span data-stu-id="8647e-109">Members</span></span>

<span data-ttu-id="8647e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8647e-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="8647e-111">[entrada] Marcas para determinar el comportamiento adecuado durante la descarga.</span><span class="sxs-lookup"><span data-stu-id="8647e-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="8647e-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="8647e-112">DNH_OK</span></span>
    
   - <span data-ttu-id="8647e-113">[entrada] Descarga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="8647e-113">[in] Download was successful.</span></span> <span data-ttu-id="8647e-114">El cliente establece esto después de descargar información desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="8647e-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="8647e-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="8647e-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="8647e-116">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="8647e-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="8647e-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="8647e-117">_pxihc_</span></span>
  
>  <span data-ttu-id="8647e-118">[out] Puntero a la interfaz de jerarquía de **IExchangeImportHierarchyChanges** que admite la descarga de los cambios incrementales de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="8647e-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="8647e-119">Para obtener más información sobre **IExchangeImportHierarchyChanges**, vea [Los criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="8647e-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="8647e-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="8647e-120">_cEntNew_</span></span>
  
> <span data-ttu-id="8647e-121">[out] Número de carpetas agregadas al almacén local.</span><span class="sxs-lookup"><span data-stu-id="8647e-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="8647e-122">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="8647e-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="8647e-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="8647e-123">_cEntMod_</span></span>
  
> <span data-ttu-id="8647e-124">[out] Número de carpetas que desea modificar en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="8647e-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="8647e-125">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="8647e-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="8647e-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="8647e-126">_cEntDel_</span></span>
  
> <span data-ttu-id="8647e-127">[out] Número de carpetas que desea eliminar en el almacén local.</span><span class="sxs-lookup"><span data-stu-id="8647e-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="8647e-128">Outlook rellena este valor durante la descarga al usar ICS.</span><span class="sxs-lookup"><span data-stu-id="8647e-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8647e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8647e-129">See also</span></span>

- [<span data-ttu-id="8647e-130">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="8647e-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="8647e-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8647e-131">MAPI Constants</span></span>](mapi-constants.md)

