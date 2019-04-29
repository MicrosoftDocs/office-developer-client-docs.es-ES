---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a5e508f5f7e6554a115517da87a8eac39f39aecf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412978"
---
# <a name="flaglist"></a><span data-ttu-id="fb6f4-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="fb6f4-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="fb6f4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb6f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb6f4-105">Contiene una lista de marcas utilizadas para indicar el estado de las entradas de direcciones durante el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fb6f4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="fb6f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb6f4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fb6f4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="fb6f4-108">Members</span><span class="sxs-lookup"><span data-stu-id="fb6f4-108">Members</span></span>

 <span data-ttu-id="fb6f4-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="fb6f4-109">**cFlags**</span></span>
  
> <span data-ttu-id="fb6f4-110">Número de marcas definidas por MAPI en la lista.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="fb6f4-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="fb6f4-111">**ulFlags**</span></span>
  
> <span data-ttu-id="fb6f4-112">Matriz de marcadores que proporciona el estado de la operación de resolución de nombres para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="fb6f4-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="fb6f4-113">The following flags can be set:</span></span>
    
<span data-ttu-id="fb6f4-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="fb6f4-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="fb6f4-115">Se ha resuelto el destinatario, pero no un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="fb6f4-116">Otros contenedores de libretas de direcciones no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="fb6f4-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="fb6f4-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="fb6f4-118">El destinatario se ha resuelto en un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="fb6f4-119">Otros contenedores de libretas de direcciones no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="fb6f4-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="fb6f4-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="fb6f4-121">La entrada no se ha resuelto.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-121">The entry has not been resolved.</span></span> <span data-ttu-id="fb6f4-122">Otros contenedores de libretas de direcciones deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb6f4-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb6f4-123">Remarks</span></span>

<span data-ttu-id="fb6f4-124">La estructura **FLAGLIST** se usa como parámetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="fb6f4-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="fb6f4-125">Cada uno de los destinatarios que se van a resolver se incluye en una estructura [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="fb6f4-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="fb6f4-126">Como el contenedor de la libreta de direcciones intenta resolver cada destinatario, establece la marca correspondiente en la entrada correspondiente de la estructura **FLAGLIST** .</span><span class="sxs-lookup"><span data-stu-id="fb6f4-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="fb6f4-127">Todas las entradas de la estructura **FLAGLIST** están en el mismo orden que las entradas de la estructura **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="fb6f4-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="fb6f4-128">Esto hace que sea más fácil asociar una configuración de marca a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="fb6f4-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fb6f4-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="fb6f4-129">See also</span></span>



[<span data-ttu-id="fb6f4-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="fb6f4-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="fb6f4-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="fb6f4-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="fb6f4-132">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="fb6f4-132">MAPI Structures</span></span>](mapi-structures.md)

