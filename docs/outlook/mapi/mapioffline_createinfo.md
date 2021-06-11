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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429568"
---
# <a name="mapioffline_createinfo"></a><span data-ttu-id="f822e-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="f822e-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="f822e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f822e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f822e-105">Esta estructura se usa con [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="f822e-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="f822e-106">Members</span><span class="sxs-lookup"><span data-stu-id="f822e-106">Members</span></span>

 <span data-ttu-id="f822e-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="f822e-107">**ulSize**</span></span>
  
> <span data-ttu-id="f822e-108">El tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="f822e-108">The size of structure.</span></span>
    
 <span data-ttu-id="f822e-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="f822e-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="f822e-110">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="f822e-110">It must be 0.</span></span>
    
 <span data-ttu-id="f822e-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="f822e-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="f822e-112">Nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="f822e-112">The name of the profile.</span></span>
    
 <span data-ttu-id="f822e-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f822e-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="f822e-114">Máscara de bits de las siguientes marcas de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="f822e-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="f822e-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="f822e-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="f822e-116">El objeto sin conexión es capaz de desconectarse.</span><span class="sxs-lookup"><span data-stu-id="f822e-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="f822e-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="f822e-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="f822e-118">El objeto sin conexión es capaz de ponerse en línea.</span><span class="sxs-lookup"><span data-stu-id="f822e-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="f822e-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="f822e-119">**pGUID**</span></span>
  
> <span data-ttu-id="f822e-120">Puntero a un GUID que se usa para identificar de forma única este tipo de objeto sin conexión desde otros objetos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f822e-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="f822e-121">GUID_GlobalState hace referencia al objeto sin conexión global que los objetos pueden usar como objeto primario.</span><span class="sxs-lookup"><span data-stu-id="f822e-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="f822e-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="f822e-122">**pInstance**</span></span>
  
> <span data-ttu-id="f822e-123">Puntero al GUID que identifica de forma exclusiva este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f822e-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="f822e-124">Se usa para desambiguar estos objetos sin conexión de otros objetos.</span><span class="sxs-lookup"><span data-stu-id="f822e-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="f822e-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="f822e-125">**pParent**</span></span>
  
> <span data-ttu-id="f822e-126">Puntero al objeto sin conexión que es el elemento primario de este objeto sin conexión y cuyos cambios heredará este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f822e-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="f822e-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="f822e-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="f822e-128">Identifica el objeto de soporte técnico MAPI que usará este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f822e-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="f822e-129">Por ejemplo, si este objeto sin conexión se usa para realizar un seguimiento del estado sin conexión y en línea de un almacén, este es el objeto de soporte de almacenes.</span><span class="sxs-lookup"><span data-stu-id="f822e-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="f822e-130">Sin embargo, si se trata de un objeto sin conexión para un objeto sin ningún objeto de soporte, puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f822e-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="f822e-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="f822e-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="f822e-132">Puntero a una MAPIOFFLINE_AGGREGATEINFO estructura.</span><span class="sxs-lookup"><span data-stu-id="f822e-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="f822e-133">Para obtener más información, [vea MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="f822e-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="f822e-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="f822e-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="f822e-135">Debe ser null.</span><span class="sxs-lookup"><span data-stu-id="f822e-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f822e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f822e-136">See also</span></span>



[<span data-ttu-id="f822e-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="f822e-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="f822e-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="f822e-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

