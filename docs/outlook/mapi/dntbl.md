---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398125"
---
# <a name="dntbl"></a><span data-ttu-id="1633d-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="1633d-103">DNTBL</span></span>
 
<span data-ttu-id="1633d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1633d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1633d-105">Información para descargar el contenido de una carpeta del servidor durante el [estado descargar tabla](download-table-state.md), como parte de una sincronización completa para el contenido de un almacén.</span><span class="sxs-lookup"><span data-stu-id="1633d-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1633d-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1633d-106">Quick Info</span></span>

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a><span data-ttu-id="1633d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1633d-107">Members</span></span>

<span data-ttu-id="1633d-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1633d-108">_ulFlags_</span></span>
  
> <span data-ttu-id="1633d-109">[entrada] Marcadores para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="1633d-109">[in] Flags to modify behavior.</span></span> 
    
  - <span data-ttu-id="1633d-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="1633d-110">DNT_OK</span></span>
    
    - <span data-ttu-id="1633d-111">[entrada] La descarga se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1633d-111">[in] Download was successful.</span></span> <span data-ttu-id="1633d-112">El cliente lo establece después de descargar la información del servidor.</span><span class="sxs-lookup"><span data-stu-id="1633d-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="1633d-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="1633d-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="1633d-114">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="1633d-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="1633d-116">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="1633d-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="1633d-118">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="1633d-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="1633d-120">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="1633d-121">_pxicc_</span></span>
  
>  <span data-ttu-id="1633d-122">[salida] Puntero a la interfaz de contenido **IExchangeImportContentsChanges** que admite la descarga de cambios en el contenido.</span><span class="sxs-lookup"><span data-stu-id="1633d-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="1633d-123">Para más información sobre **IExchangeImportContentsChanges**, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1633d-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="1633d-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="1633d-124">_pxihc_</span></span>
  
>  <span data-ttu-id="1633d-125">[salida] Puntero a la interfaz de contenido **IExchangeImportHierarchyChanges** que admite la descarga de los cambios de jerarquía incremental.</span><span class="sxs-lookup"><span data-stu-id="1633d-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="1633d-126">Para más información sobre **IExchangeImportHierarchyChanges**, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1633d-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="1633d-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="1633d-127">_pszName_</span></span>
  
>  <span data-ttu-id="1633d-128">[salida] Nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1633d-128">Name of the folder.</span></span> 
    
<span data-ttu-id="1633d-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="1633d-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="1633d-130">[salida] Última vez que se modificó la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1633d-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="1633d-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="1633d-131">_ulRights_</span></span>
  
>  <span data-ttu-id="1633d-132">[salida] Valor de la propiedad **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1633d-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="1633d-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="1633d-133">_FEID_</span></span>
  
>  <span data-ttu-id="1633d-134">[salida] Id. de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="1633d-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="1633d-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="1633d-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="1633d-136">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="1633d-137">_rgte_</span></span>
  
> <span data-ttu-id="1633d-138">[salida] Cambios de elementos normales (o no ocultos) y asociados (ocultos).</span><span class="sxs-lookup"><span data-stu-id="1633d-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="1633d-139">*rgte[0]* es para elementos normales y *rgte[1]* para elementos asociados.</span><span class="sxs-lookup"><span data-stu-id="1633d-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="1633d-140">Outlook rellena este miembro durante la descarga al usar la sincronización de cambio incremental (ICS).</span><span class="sxs-lookup"><span data-stu-id="1633d-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="1633d-141">Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="1633d-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="1633d-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="1633d-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="1633d-143">[entrada] / [salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="1633d-144">_boReserved_</span></span>
  
>  <span data-ttu-id="1633d-145">[entrada] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="1633d-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="1633d-147">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1633d-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="1633d-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="1633d-149">[entrada] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1633d-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1633d-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="1633d-150">See also</span></span>

- [<span data-ttu-id="1633d-151">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="1633d-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="1633d-152">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="1633d-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="1633d-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="1633d-153">DNTBLE</span></span>](dntble.md)

