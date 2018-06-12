---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 17ab26c62bcbb57ff8e53b5412ca27ed414fb725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818265"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="1ecb9-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="1ecb9-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="1ecb9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ecb9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ecb9-105">Esta estructura se utiliza con [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="1ecb9-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="1ecb9-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1ecb9-106">Members</span></span>

 <span data-ttu-id="1ecb9-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-107">**ulSize**</span></span>
  
> <span data-ttu-id="1ecb9-108">El tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-108">The size of structure.</span></span>
    
 <span data-ttu-id="1ecb9-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="1ecb9-110">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-110">It must be 0.</span></span>
    
 <span data-ttu-id="1ecb9-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="1ecb9-112">Nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-112">The name of the profile.</span></span>
    
 <span data-ttu-id="1ecb9-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="1ecb9-114">Una máscara de bits de los siguientes indicadores de capacidad.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="1ecb9-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="1ecb9-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="1ecb9-116">El objeto sin conexión es capaz de trabajar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="1ecb9-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="1ecb9-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="1ecb9-118">El objeto sin conexión es capaz de conectarse.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="1ecb9-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-119">**pGUID**</span></span>
  
> <span data-ttu-id="1ecb9-120">Puntero a un GUID que se utiliza para identificar de forma exclusiva este tipo de objeto sin conexión desde otros objetos sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="1ecb9-121">GUID_GlobalState hace referencia al objeto global sin conexión que los objetos pueden usar como un objeto primario.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="1ecb9-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-122">**pInstance**</span></span>
  
> <span data-ttu-id="1ecb9-123">Puntero al GUID que identifica de forma exclusiva este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="1ecb9-124">Se usa para eliminar la ambigüedad de esta objetos sin conexión desde otros objetos.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="1ecb9-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-125">**pParent**</span></span>
  
> <span data-ttu-id="1ecb9-126">Puntero al objeto sin conexión que es el elemento primario de este objeto sin conexión y cuyos cambios heredará este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="1ecb9-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="1ecb9-128">Identifica el objeto de soporte técnico MAPI que usará este objeto sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="1ecb9-129">Por ejemplo, si este objeto sin conexión se usa para realizar un seguimiento de un almacén sin conexión y el estado en línea, a continuación, esto es los almacenes admiten el objeto.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="1ecb9-130">Sin embargo, si se trata de un objeto sin conexión para un objeto con ningún objeto de soporte técnico, a continuación, puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="1ecb9-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="1ecb9-132">Un puntero a una estructura MAPIOFFLINE_AGGREGATEINFO.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="1ecb9-133">Para obtener más información, vea [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="1ecb9-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="1ecb9-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="1ecb9-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="1ecb9-135">Debe ser null.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ecb9-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="1ecb9-136">See also</span></span>



[<span data-ttu-id="1ecb9-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="1ecb9-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="1ecb9-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="1ecb9-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

