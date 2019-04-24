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
# <a name="upmov"></a><span data-ttu-id="30ba0-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="30ba0-103">UPMOV</span></span>
 
<span data-ttu-id="30ba0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30ba0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30ba0-105">Información para cargar los elementos que se han movido.</span><span class="sxs-lookup"><span data-stu-id="30ba0-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="30ba0-106">Esta información se usa durante el estado de [carga de eliminación](upload-delete-status-state.md) y carga de la [tabla](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="30ba0-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30ba0-107">Información rápida</span><span class="sxs-lookup"><span data-stu-id="30ba0-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="30ba0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="30ba0-108">Members</span></span>

<span data-ttu-id="30ba0-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30ba0-109">_ulFlags_</span></span>
  
> <span data-ttu-id="30ba0-110">a Marcas para determinar el comportamiento adecuado durante la carga.</span><span class="sxs-lookup"><span data-stu-id="30ba0-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="30ba0-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="30ba0-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="30ba0-112">a Problema al abrir la carpeta del servidor.</span><span class="sxs-lookup"><span data-stu-id="30ba0-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="30ba0-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="30ba0-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="30ba0-114">a El estado de carga ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="30ba0-114">[in] The upload state has changed.</span></span> <span data-ttu-id="30ba0-115">El cliente lo usa para realizar un seguimiento del cambio en el estado del almacén local.</span><span class="sxs-lookup"><span data-stu-id="30ba0-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="30ba0-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="30ba0-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="30ba0-117">a Estado de carga de confirmación.</span><span class="sxs-lookup"><span data-stu-id="30ba0-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="30ba0-118">_Preserva_</span><span class="sxs-lookup"><span data-stu-id="30ba0-118">_pReserved_</span></span>
  
>  <span data-ttu-id="30ba0-119">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="30ba0-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="30ba0-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="30ba0-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="30ba0-121">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="30ba0-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="30ba0-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="30ba0-122">_pszName_</span></span>
  
>  <span data-ttu-id="30ba0-123">contempla Nombre de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="30ba0-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="30ba0-124">Este miembro no es compatible con uniCODE.</span><span class="sxs-lookup"><span data-stu-id="30ba0-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="30ba0-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="30ba0-125">_feid_</span></span>
  
>  <span data-ttu-id="30ba0-126">contempla IDENTIFICADOR de entrada de la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="30ba0-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="30ba0-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="30ba0-127">_pfld_</span></span>
  
>  <span data-ttu-id="30ba0-128">a Puntero a la carpeta del servidor.</span><span class="sxs-lookup"><span data-stu-id="30ba0-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="30ba0-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="30ba0-129">_pxicc_</span></span>
  
>  <span data-ttu-id="30ba0-130">a Puntero a la interfaz de contenido **IExchangeImportContentsChanges** que admite la carga de cambios de contenido al usar la sincronización de cambio incremental (ICS).</span><span class="sxs-lookup"><span data-stu-id="30ba0-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="30ba0-131">Para obtener más información acerca de **IExchangeImportContentsChanges** e ICS, consulte [criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="30ba0-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="30ba0-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="30ba0-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="30ba0-133">[salida] Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="30ba0-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="30ba0-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="30ba0-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="30ba0-135">contempla Siguiente contexto de movimiento.</span><span class="sxs-lookup"><span data-stu-id="30ba0-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="30ba0-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="30ba0-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="30ba0-137">a Número de elementos movidos aquí.</span><span class="sxs-lookup"><span data-stu-id="30ba0-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="30ba0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="30ba0-138">See also</span></span>

- [<span data-ttu-id="30ba0-139">Información sobre la API de replicación</span><span class="sxs-lookup"><span data-stu-id="30ba0-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="30ba0-140">Información sobre la máquina de estados de replicación</span><span class="sxs-lookup"><span data-stu-id="30ba0-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="30ba0-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="30ba0-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="30ba0-142">FEID</span><span class="sxs-lookup"><span data-stu-id="30ba0-142">FEID</span></span>](feid.md)

