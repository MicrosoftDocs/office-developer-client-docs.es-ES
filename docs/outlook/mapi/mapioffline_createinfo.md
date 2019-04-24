---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357130"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="201fb-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="201fb-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="201fb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="201fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="201fb-105">Esta estructura se usa con [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="201fb-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a><span data-ttu-id="201fb-106">Members</span><span class="sxs-lookup"><span data-stu-id="201fb-106">Members</span></span>

 <span data-ttu-id="201fb-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="201fb-107">**ulSize**</span></span>
  
> <span data-ttu-id="201fb-108">El tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="201fb-108">The size of structure.</span></span>
    
 <span data-ttu-id="201fb-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="201fb-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="201fb-110">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="201fb-110">It must be 0.</span></span>
    
 <span data-ttu-id="201fb-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="201fb-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="201fb-112">Nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="201fb-112">The name of the profile.</span></span>
    
 <span data-ttu-id="201fb-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="201fb-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="201fb-114">Máscara de bits de las siguientes marcas de capacidad.</span><span class="sxs-lookup"><span data-stu-id="201fb-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="201fb-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="201fb-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="201fb-116">El objeto sin conexión puede desconectarse.</span><span class="sxs-lookup"><span data-stu-id="201fb-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="201fb-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="201fb-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="201fb-118">El objeto sin conexión puede pasar a estar en línea.</span><span class="sxs-lookup"><span data-stu-id="201fb-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="201fb-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="201fb-119">**pGUID**</span></span>
  
> <span data-ttu-id="201fb-120">Puntero a un GUID que se usa para identificar de forma única este tipo de objeto sin conexión de otros objetos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="201fb-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="201fb-121">GUID_GlobalState hace referencia al objeto global sin conexión que los objetos pueden usar como objeto primario.</span><span class="sxs-lookup"><span data-stu-id="201fb-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="201fb-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="201fb-122">**pInstance**</span></span>
  
> <span data-ttu-id="201fb-123">Puntero a GUID que identifica de forma única este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="201fb-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="201fb-124">Se usa para eliminar la ambigüedad de los objetos sin conexión de otros objetos.</span><span class="sxs-lookup"><span data-stu-id="201fb-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="201fb-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="201fb-125">**pParent**</span></span>
  
> <span data-ttu-id="201fb-126">Puntero a objeto sin conexión que es el elemento principal de este objeto sin conexión y cuyos cambios heredará este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="201fb-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="201fb-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="201fb-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="201fb-128">Identifica el objeto compatible con MAPI que usará este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="201fb-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="201fb-129">Por ejemplo, si este objeto sin conexión se usa para realizar un seguimiento del estado de conexión y de conexión de un almacén, este es el objeto de soporte de almacenes.</span><span class="sxs-lookup"><span data-stu-id="201fb-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="201fb-130">Sin embargo, si se trata de un objeto sin conexión para un objeto que no es compatible con el objeto, puede ser nulo.</span><span class="sxs-lookup"><span data-stu-id="201fb-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="201fb-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="201fb-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="201fb-132">Un puntero a una estructura MAPIOFFLINE_AGGREGATEINFO.</span><span class="sxs-lookup"><span data-stu-id="201fb-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="201fb-133">Para obtener más información, vea [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="201fb-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="201fb-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="201fb-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="201fb-135">Debe ser null.</span><span class="sxs-lookup"><span data-stu-id="201fb-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="201fb-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="201fb-136">See also</span></span>



[<span data-ttu-id="201fb-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="201fb-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="201fb-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="201fb-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

