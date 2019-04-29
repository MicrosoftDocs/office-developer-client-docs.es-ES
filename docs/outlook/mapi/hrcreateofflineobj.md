---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0a34c441a473154a43a107b4236ccc259d327dba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414392"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="71390-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="71390-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="71390-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71390-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="71390-105">Crea un objeto MAPI sin conexión que utiliza el proveedor y el almacén para notificar a MAPI Cuándo el objeto se conecta y se desconecta,</span><span class="sxs-lookup"><span data-stu-id="71390-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71390-106">ExPortado por:</span><span class="sxs-lookup"><span data-stu-id="71390-106">Exported by:</span></span>  <br/> |<span data-ttu-id="71390-107">Msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="71390-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="71390-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="71390-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="71390-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="71390-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="71390-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="71390-110">Called by:</span></span>  <br/> |<span data-ttu-id="71390-111">Client</span><span class="sxs-lookup"><span data-stu-id="71390-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="71390-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="71390-112">Parameters</span></span>

<span data-ttu-id="71390-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="71390-113">_ulFlags_</span></span>
  
> <span data-ttu-id="71390-114">a Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="71390-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="71390-115">_pCreateInfo_</span><span class="sxs-lookup"><span data-stu-id="71390-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="71390-116">a Un puntero a una estructura **MAPIOFFLINE_CREATEINFO** que contiene la información necesaria para crear el objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="71390-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="71390-117">_ppOffline_</span><span class="sxs-lookup"><span data-stu-id="71390-117">_ppOffline_</span></span>
  
> <span data-ttu-id="71390-118">contempla Un puntero a la interfaz **IMAPIOfflineMgr** .</span><span class="sxs-lookup"><span data-stu-id="71390-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="71390-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71390-119">Return value</span></span>

<span data-ttu-id="71390-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="71390-120">None.</span></span>
  
<span data-ttu-id="71390-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="71390-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="71390-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71390-122">Example</span></span>

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a><span data-ttu-id="71390-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="71390-123">See also</span></span>

- [<span data-ttu-id="71390-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="71390-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="71390-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="71390-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

