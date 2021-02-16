---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432208"
---
# <a name="mapiuid"></a><span data-ttu-id="40cf2-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="40cf2-103">MAPIUID</span></span>

  
  
<span data-ttu-id="40cf2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40cf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40cf2-105">Una versión independiente de orden de bytes de una [estructura GUID](guid.md) que se usa para identificar de forma única un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="40cf2-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40cf2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="40cf2-106">Header file:</span></span>  <br/> |<span data-ttu-id="40cf2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="40cf2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="40cf2-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="40cf2-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="40cf2-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="40cf2-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="40cf2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="40cf2-110">Members</span></span>

 <span data-ttu-id="40cf2-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="40cf2-111">**ab**</span></span>
  
> <span data-ttu-id="40cf2-112">Matriz que contiene un identificador de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="40cf2-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="40cf2-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="40cf2-113">Remarks</span></span>

<span data-ttu-id="40cf2-114">Una **estructura MAPIUID** es una **estructura GUID** que se coloca en el orden de bytes ® procesador Intel.</span><span class="sxs-lookup"><span data-stu-id="40cf2-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="40cf2-115">MAPI crea **estructuras MAPIUID** de una manera que hace muy raro que dos elementos diferentes tengan el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="40cf2-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="40cf2-116">**Las estructuras MAPIUID** se pueden almacenar como propiedades binarias o como archivos, sin tener en cuenta el orden de bytes del equipo que almacena o obtiene acceso a la información.</span><span class="sxs-lookup"><span data-stu-id="40cf2-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="40cf2-117">**Se usan estructuras MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="40cf2-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="40cf2-118">Para identificar una sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="40cf2-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="40cf2-119">En los identificadores de entrada del almacén de mensajes y de los objetos de la libreta de direcciones para identificar al proveedor de servicios responsable.</span><span class="sxs-lookup"><span data-stu-id="40cf2-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="40cf2-120">En la **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="40cf2-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="40cf2-121">Para generar un **identificador MAPIUID** para una clave de búsqueda, los proveedores de servicios llaman a [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="40cf2-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="40cf2-122">Cuando un cliente transmite un mensaje a través de una red, debe usar un protocolo o formato de transmisión que no cambie el orden de bytes de los datos **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="40cf2-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="40cf2-123">Para obtener más información acerca de cómo se usan las **estructuras MAPIUID,** vea los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="40cf2-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="40cf2-124">Registro de identificadores únicos del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="40cf2-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="40cf2-125">Establecer el orden de transporte</span><span class="sxs-lookup"><span data-stu-id="40cf2-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="40cf2-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="40cf2-126">See also</span></span>



[<span data-ttu-id="40cf2-127">GUID</span><span class="sxs-lookup"><span data-stu-id="40cf2-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="40cf2-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="40cf2-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="40cf2-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="40cf2-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="40cf2-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="40cf2-130">MAPI Structures</span></span>](mapi-structures.md)

