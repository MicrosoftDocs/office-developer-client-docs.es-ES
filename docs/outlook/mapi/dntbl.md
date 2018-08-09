---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816721"
---
# <a name="dntbl"></a><span data-ttu-id="df096-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="df096-103">DNTBL</span></span>
 
<span data-ttu-id="df096-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df096-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df096-105">Información para descargar el contenido de una carpeta del servidor durante el [estado de la tabla de descarga](download-table-state.md), como parte de una sincronización completa para el contenido en un almacén.</span><span class="sxs-lookup"><span data-stu-id="df096-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="df096-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="df096-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="df096-107">Members</span><span class="sxs-lookup"><span data-stu-id="df096-107">Members</span></span>

<span data-ttu-id="df096-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="df096-108">_ulFlags_</span></span>
  
> <span data-ttu-id="df096-109">[entrada] Indicadores para modificar el comportamiento</span><span class="sxs-lookup"><span data-stu-id="df096-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="df096-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="df096-110">DNT_OK</span></span>
    
    - <span data-ttu-id="df096-111">[entrada] Descarga fue correcta.</span><span class="sxs-lookup"><span data-stu-id="df096-111">[in] Download was successful.</span></span> <span data-ttu-id="df096-112">El cliente establece esto después de descargar información desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="df096-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="df096-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="df096-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="df096-114">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="df096-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="df096-116">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="df096-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="df096-118">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="df096-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="df096-120">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="df096-121">_pxicc_</span></span>
  
>  <span data-ttu-id="df096-122">[out] Puntero a la interfaz de contenido de **IExchangeImportContentsChanges** que admite la descarga de cambios en el contenido.</span><span class="sxs-lookup"><span data-stu-id="df096-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="df096-123">Para obtener más información sobre **IExchangeImportContentsChanges**, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="df096-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="df096-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="df096-124">_pxihc_</span></span>
  
>  <span data-ttu-id="df096-125">[out] Puntero a la interfaz de jerarquía de **IExchangeImportHierarchyChanges** que admite la descarga de los cambios incrementales de jerarquía.</span><span class="sxs-lookup"><span data-stu-id="df096-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="df096-126">Para obtener más información sobre **IExchangeImportHierarchyChanges**, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="df096-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="df096-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="df096-127">_pszName_</span></span>
  
>  <span data-ttu-id="df096-128">[out] Nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="df096-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="df096-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="df096-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="df096-130">[out] Hora de última modificación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="df096-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="df096-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="df096-131">_ulRights_</span></span>
  
>  <span data-ttu-id="df096-132">[out] Valor de la propiedad **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="df096-132">[out] Value of the **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="df096-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="df096-133">_feid_</span></span>
  
>  <span data-ttu-id="df096-134">[out] Identificador de entrada de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="df096-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="df096-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="df096-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="df096-136">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="df096-137">_rgte_</span></span>
  
> <span data-ttu-id="df096-138">[out] Los cambios de normal (o no ocultos) y elementos asociados (u ocultos).</span><span class="sxs-lookup"><span data-stu-id="df096-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="df096-139">*rgte [0]* es para los elementos normales y *rgte [1]* es para los elementos asociados.</span><span class="sxs-lookup"><span data-stu-id="df096-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="df096-140">Outlook rellena a este miembro durante la descarga, cuando se usa la sincronización de cambio Incremental (ICS).</span><span class="sxs-lookup"><span data-stu-id="df096-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="df096-141">Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="df096-141">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="df096-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="df096-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="df096-143">[en] / [out] este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="df096-144">_boReserved_</span></span>
  
>  <span data-ttu-id="df096-145">[entrada] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="df096-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="df096-147">[out] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="df096-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="df096-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="df096-149">[entrada] Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="df096-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="df096-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="df096-150">See also</span></span>

- [<span data-ttu-id="df096-151">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="df096-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="df096-152">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="df096-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="df096-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="df096-153">DNTBLE</span></span>](dntble.md)

