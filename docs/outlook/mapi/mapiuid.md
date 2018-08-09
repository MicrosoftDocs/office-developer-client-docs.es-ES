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
ms.openlocfilehash: 3675c6a8ee2ee208f175dd5f7d219447aa52e9ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818294"
---
# <a name="mapiuid"></a><span data-ttu-id="a098a-103">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a098a-103">MAPIUID</span></span>

  
  
<span data-ttu-id="a098a-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a098a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a098a-105">Una versión independiente de orden de bytes de una estructura [GUID](guid.md) que se utiliza para identificar de forma única un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="a098a-105">A byte-order independent version of a [GUID](guid.md) structure that is used to uniquely identify a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a098a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a098a-106">Header file:</span></span>  <br/> |<span data-ttu-id="a098a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a098a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a098a-108">Macro relacionado:</span><span class="sxs-lookup"><span data-stu-id="a098a-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="a098a-109">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="a098a-109">IsEqualMAPIUID</span></span>](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a><span data-ttu-id="a098a-110">Members</span><span class="sxs-lookup"><span data-stu-id="a098a-110">Members</span></span>

 <span data-ttu-id="a098a-111">**AB**</span><span class="sxs-lookup"><span data-stu-id="a098a-111">**ab**</span></span>
  
> <span data-ttu-id="a098a-112">Una matriz que contiene un identificador de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="a098a-112">An array that contains a 16-byte identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a098a-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a098a-113">Remarks</span></span>

<span data-ttu-id="a098a-114">Una estructura **MAPIUID** es una estructura **GUID** poner en orden de bytes del procesador de Intel®.</span><span class="sxs-lookup"><span data-stu-id="a098a-114">A **MAPIUID** structure is a **GUID** structure put into Intel® processor byte order.</span></span> 
  
<span data-ttu-id="a098a-115">MAPI crea **MAPIUID** estructuras de una manera que hace que sea muy raro que dos elementos diferentes que tienen el mismo identificador.</span><span class="sxs-lookup"><span data-stu-id="a098a-115">MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier.</span></span> <span data-ttu-id="a098a-116">Estructuras **MAPIUID** pueden almacenarse como propiedades binarias o como archivos, sin tener en cuenta el orden de bytes del equipo almacenar y acceder a la información.</span><span class="sxs-lookup"><span data-stu-id="a098a-116">**MAPIUID** structures can be stored as binary properties or as files, without regard to the byte ordering of the computer storing or accessing the information.</span></span> 
  
 <span data-ttu-id="a098a-117">Se usan las estructuras **MAPIUID** :</span><span class="sxs-lookup"><span data-stu-id="a098a-117">**MAPIUID** structures are used:</span></span> 
  
- <span data-ttu-id="a098a-118">Para identificar una sección de perfil.</span><span class="sxs-lookup"><span data-stu-id="a098a-118">To identify a profile section.</span></span>
    
- <span data-ttu-id="a098a-119">En la entrada de identificadores de mensaje de almacenan y objetos de la libreta para identificar el proveedor de servicio responsable de direcciones.</span><span class="sxs-lookup"><span data-stu-id="a098a-119">In the entry identifiers of message store and address book objects to identify the responsible service provider.</span></span>
    
- <span data-ttu-id="a098a-120">En la propiedad **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="a098a-120">In the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of messages.</span></span>
    
<span data-ttu-id="a098a-121">Para generar un identificador **MAPIUID** para una clave de búsqueda, proveedores de servicios de llamar a [IMAPISupport::NewUID](imapisupport-newuid.md).</span><span class="sxs-lookup"><span data-stu-id="a098a-121">To generate a **MAPIUID** identifier for a search key, service providers call [IMAPISupport::NewUID](imapisupport-newuid.md).</span></span>
  
<span data-ttu-id="a098a-122">Cuando un cliente transmite un mensaje a través de una red, debe utilizar un formato de transmisión o de protocolo que no cambia el orden de bytes de datos **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="a098a-122">When a client transmits a message across a network, it should use a protocol or transmission format that does not change the byte order of **MAPIUID** data.</span></span> 
  
<span data-ttu-id="a098a-123">Para obtener más información acerca de cómo se usan las estructuras **MAPIUID** , consulte los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a098a-123">For more information about how **MAPIUID** structures are used, see the following topics:</span></span> 
  
[<span data-ttu-id="a098a-124">Registrar identificadores únicos del proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="a098a-124">Registering Service Provider Unique Identifiers</span></span>](registering-service-provider-unique-identifiers.md)
  
[<span data-ttu-id="a098a-125">Establecer el orden de transporte</span><span class="sxs-lookup"><span data-stu-id="a098a-125">Setting Transport Order</span></span>](setting-transport-order.md)
  
## <a name="see-also"></a><span data-ttu-id="a098a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a098a-126">See also</span></span>



[<span data-ttu-id="a098a-127">GUID</span><span class="sxs-lookup"><span data-stu-id="a098a-127">GUID</span></span>](guid.md)
  
[<span data-ttu-id="a098a-128">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="a098a-128">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="a098a-129">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="a098a-129">IMAPISupport::NewUID</span></span>](imapisupport-newuid.md)


[<span data-ttu-id="a098a-130">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="a098a-130">MAPI Structures</span></span>](mapi-structures.md)

