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
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816828"
---
# <a name="flaglist"></a><span data-ttu-id="d8fc0-103">FLAGLIST</span><span class="sxs-lookup"><span data-stu-id="d8fc0-103">FLAGLIST</span></span>

  
  
<span data-ttu-id="d8fc0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d8fc0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d8fc0-105">Contiene una lista de marcas que se usan para indicar el estado de las entradas de dirección durante el proceso de resolución de nombres.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-105">Contains a list of flags used to indicate the status of address entries during the name resolution process.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8fc0-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d8fc0-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8fc0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8fc0-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a><span data-ttu-id="d8fc0-108">Members</span><span class="sxs-lookup"><span data-stu-id="d8fc0-108">Members</span></span>

 <span data-ttu-id="d8fc0-109">**cFlags**</span><span class="sxs-lookup"><span data-stu-id="d8fc0-109">**cFlags**</span></span>
  
> <span data-ttu-id="d8fc0-110">Recuento de indicadores definidas en MAPI en la lista.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-110">Count of MAPI-defined flags in the list.</span></span>
    
 <span data-ttu-id="d8fc0-111">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d8fc0-111">**ulFlags**</span></span>
  
> <span data-ttu-id="d8fc0-112">Una matriz de marcadores que proporciona el estado de la operación de resolución de nombres para un destinatario.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-112">An array of flags that provides the status of the name resolution operation for a recipient.</span></span> <span data-ttu-id="d8fc0-113">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d8fc0-113">The following flags can be set:</span></span>
    
<span data-ttu-id="d8fc0-114">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="d8fc0-114">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="d8fc0-115">El destinatario se ha resuelto, pero no a un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-115">The recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="d8fc0-116">Otros contenedores de la libreta de direcciones no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-116">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="d8fc0-117">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="d8fc0-117">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="d8fc0-118">El destinatario se ha resuelto para un identificador de entrada único.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-118">The recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="d8fc0-119">Otros contenedores de la libreta de direcciones no deben intentar resolver este destinatario.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-119">Other address book containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="d8fc0-120">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="d8fc0-120">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="d8fc0-121">La entrada no se ha resuelta.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-121">The entry has not been resolved.</span></span> <span data-ttu-id="d8fc0-122">Otros contenedores de la libreta de direcciones deben intentar resolver a este destinatario.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-122">Other address book containers should try to resolve this recipient.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8fc0-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8fc0-123">Remarks</span></span>

<span data-ttu-id="d8fc0-124">La estructura **FLAGLIST** se usa como un parámetro para [IABContainer:: ResolveNames](iabcontainer-resolvenames.md).</span><span class="sxs-lookup"><span data-stu-id="d8fc0-124">The **FLAGLIST** structure is used as a parameter to [IABContainer::ResolveNames](iabcontainer-resolvenames.md).</span></span> <span data-ttu-id="d8fc0-125">Cada uno de los destinatarios que se puede resolver se incluye en una estructura de [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="d8fc0-125">Each of the recipients to be resolved is included in an [ADRLIST](adrlist.md) structure.</span></span> <span data-ttu-id="d8fc0-126">Como el contenedor de la libreta de direcciones intenta resolver a cada destinatario, Establece la marca adecuada en la entrada correspondiente en la estructura **FLAGLIST** .</span><span class="sxs-lookup"><span data-stu-id="d8fc0-126">As the address book container attempts to resolve each recipient, it sets the appropriate flag in the corresponding entry in the **FLAGLIST** structure.</span></span> <span data-ttu-id="d8fc0-127">Todas las entradas de la estructura de **FLAGLIST** se encuentran en el mismo orden que las entradas de la estructura de **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="d8fc0-127">All of the entries in the **FLAGLIST** structure are in the same order as the entries in the **ADRLIST** structure.</span></span> <span data-ttu-id="d8fc0-128">Esto facilita la asociar un valor de marca a un destinatario.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-128">This makes it easy to associate a flag setting with a recipient.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8fc0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8fc0-129">See also</span></span>



[<span data-ttu-id="d8fc0-130">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="d8fc0-130">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="d8fc0-131">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="d8fc0-131">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)


[<span data-ttu-id="d8fc0-132">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="d8fc0-132">MAPI Structures</span></span>](mapi-structures.md)

