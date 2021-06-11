---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339189"
---
# <a name="upmov"></a><span data-ttu-id="da9c2-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="da9c2-103">UPMOV</span></span>
 
<span data-ttu-id="da9c2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da9c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da9c2-105">Información para cargar elementos que se han movido.</span><span class="sxs-lookup"><span data-stu-id="da9c2-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="da9c2-106">Esta información se usa durante el estado [de eliminación de carga y](upload-delete-status-state.md) el estado de la tabla de [carga.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="da9c2-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="da9c2-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="da9c2-107">Quick info</span></span>

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a><span data-ttu-id="da9c2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="da9c2-108">Members</span></span>

<span data-ttu-id="da9c2-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="da9c2-109">_ulFlags_</span></span>
  
> <span data-ttu-id="da9c2-110">[in] Marcas para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="da9c2-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="da9c2-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="da9c2-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="da9c2-112">[in] Problema al abrir la carpeta del servidor.</span><span class="sxs-lookup"><span data-stu-id="da9c2-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="da9c2-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="da9c2-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="da9c2-114">[in] El estado de carga ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="da9c2-114">[in] The upload state has changed.</span></span> <span data-ttu-id="da9c2-115">El cliente lo usa para realizar un seguimiento del cambio de estado del almacén local.</span><span class="sxs-lookup"><span data-stu-id="da9c2-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="da9c2-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="da9c2-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="da9c2-117">[in] Confirmar el estado de carga.</span><span class="sxs-lookup"><span data-stu-id="da9c2-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="da9c2-118">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="da9c2-118">_pReserved_</span></span>
  
>  <span data-ttu-id="da9c2-119">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="da9c2-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="da9c2-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="da9c2-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="da9c2-121">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="da9c2-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="da9c2-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="da9c2-122">_pszName_</span></span>
  
>  <span data-ttu-id="da9c2-123">[salida] Nombre de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="da9c2-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="da9c2-124">Este miembro no admite UNICODE.</span><span class="sxs-lookup"><span data-stu-id="da9c2-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="da9c2-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="da9c2-125">_feid_</span></span>
  
>  <span data-ttu-id="da9c2-126">[salida] Id. de entrada de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="da9c2-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="da9c2-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="da9c2-127">_pfld_</span></span>
  
>  <span data-ttu-id="da9c2-128">[in] Puntero a la carpeta del servidor.</span><span class="sxs-lookup"><span data-stu-id="da9c2-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="da9c2-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="da9c2-129">_pxicc_</span></span>
  
>  <span data-ttu-id="da9c2-130">[in] Puntero a la **interfaz de contenido IExchangeImportContentsChanges** que admite la carga de cambios de contenido al usar la sincronización incremental de cambios (ICS).</span><span class="sxs-lookup"><span data-stu-id="da9c2-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="da9c2-131">Para obtener más información **sobre IExchangeImportContentsChanges** e ICS, vea [Criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="da9c2-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="da9c2-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="da9c2-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="da9c2-133">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="da9c2-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="da9c2-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="da9c2-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="da9c2-135">[salida] Siguiente contexto de movimiento.</span><span class="sxs-lookup"><span data-stu-id="da9c2-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="da9c2-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="da9c2-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="da9c2-137">[in] Número de elementos movidos aquí.</span><span class="sxs-lookup"><span data-stu-id="da9c2-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="da9c2-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="da9c2-138">See also</span></span>

- [<span data-ttu-id="da9c2-139">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="da9c2-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="da9c2-140">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="da9c2-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="da9c2-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="da9c2-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="da9c2-142">FEID</span><span class="sxs-lookup"><span data-stu-id="da9c2-142">FEID</span></span>](feid.md)

