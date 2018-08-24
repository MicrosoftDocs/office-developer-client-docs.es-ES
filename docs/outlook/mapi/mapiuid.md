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
ms.openlocfilehash: f7ec60768ab07c56969f538f196a1f9df5dbed17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587169"
---
# <a name="mapiuid"></a><span data-ttu-id="7f5fc-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="7f5fc-103">MAPIUID</span></span>

  
  
<span data-ttu-id="7f5fc-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f5fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f5fc-105">Una versión independiente de orden de bytes de una estructura [GUID](guid.md) que se utiliza para identificar de forma única un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f5fc-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="7f5fc-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f5fc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f5fc-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="7f5fc-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="7f5fc-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="7f5fc-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="7f5fc-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="7f5fc-110">Members</span><span class="sxs-lookup"><span data-stu-id="7f5fc-110">Members</span></span>

 <span data-ttu-id="7f5fc-111">**AB**</span><span class="sxs-lookup"><span data-stu-id="7f5fc-111">**ab**</span></span>
  
> <span data-ttu-id="7f5fc-112">Una matriz que contiene un identificador de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f5fc-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7f5fc-113">Remarks</span></span>

<span data-ttu-id="7f5fc-114">Una estructura **MAPIUID** es una estructura **GUID** poner en orden de bytes del procesador de Intel®.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="7f5fc-115">MAPI crea **MAPIUID** estructuras de una manera que hace que sea muy raro que dos elementos diferentes que tienen el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="7f5fc-116">Estructuras **MAPIUID** pueden almacenarse como propiedades binarias o como archivos, sin tener en cuenta el orden de bytes del equipo almacenar y acceder a la información.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="7f5fc-117">Se usan las estructuras **MAPIUID** :</span><span class="sxs-lookup"><span data-stu-id="7f5fc-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="7f5fc-118">Para identificar una sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="7f5fc-119">En la entrada de identificadores de mensaje de almacenan y objetos de la libreta para identificar el proveedor de servicio responsable de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="7f5fc-120">En la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="7f5fc-121">Para generar un identificador **MAPIUID** para una clave de búsqueda, proveedores de servicios de llamar a [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="7f5fc-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="7f5fc-122">Cuando un cliente transmite un mensaje a través de una red, debe utilizar un formato de transmisión o de protocolo que no cambia el orden de bytes de datos **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="7f5fc-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="7f5fc-123">Para obtener más información acerca de cómo se usan las estructuras **MAPIUID** , consulte los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="7f5fc-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="7f5fc-124">Registrar identificadores únicos del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="7f5fc-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="7f5fc-125">Establecer el orden de transporte</span><span class="sxs-lookup"><span data-stu-id="7f5fc-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="7f5fc-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f5fc-126">See also</span></span>



[<span data-ttu-id="7f5fc-127">GUID</span><span class="sxs-lookup"><span data-stu-id="7f5fc-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="7f5fc-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="7f5fc-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="7f5fc-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="7f5fc-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="7f5fc-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="7f5fc-130">MAPI Structures</span></span>](mapi-structures.md)

