---
title: Propiedad canónica PidTagRpcOverHttpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c8b30768-cf83-450d-9fe2-567a5e0c2f57
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cf1f3b4d72426fb5f80decdc074a622b140657c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327450"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="21f81-103">Propiedad canónica PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="21f81-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="21f81-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21f81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21f81-105">Contiene la configuración de un perfil usado por Microsoft Office Outlook para conectarse a Microsoft Exchange Server mediante una llamada de procedimiento remoto (RPC) a través del protocolo de transferencia de hipertexto (HTTP).</span><span class="sxs-lookup"><span data-stu-id="21f81-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21f81-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="21f81-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21f81-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="21f81-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="21f81-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="21f81-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21f81-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="21f81-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="21f81-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="21f81-110">Data type:</span></span>  <br/> |<span data-ttu-id="21f81-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="21f81-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="21f81-112">Área:</span><span class="sxs-lookup"><span data-stu-id="21f81-112">Area:</span></span>  <br/> |<span data-ttu-id="21f81-113">Varios</span><span class="sxs-lookup"><span data-stu-id="21f81-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21f81-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="21f81-114">Remarks</span></span>

<span data-ttu-id="21f81-115">La **PR_ROH_FLAGS** se almacena en la sección Perfil global de un perfil de interfaz de programación de aplicaciones de mensajería (MAPI).</span><span class="sxs-lookup"><span data-stu-id="21f81-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="21f81-116">El valor **de PR_ROH_FLAGS** es una máscara de bits que está hecha de una o más de las siguientes marcas.</span><span class="sxs-lookup"><span data-stu-id="21f81-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="21f81-117">**Name**</span><span class="sxs-lookup"><span data-stu-id="21f81-117">**Name**</span></span>|<span data-ttu-id="21f81-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="21f81-118">**Value**</span></span>|<span data-ttu-id="21f81-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="21f81-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21f81-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="21f81-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="21f81-121">0x1</span><span class="sxs-lookup"><span data-stu-id="21f81-121">0x1</span></span>  <br/> |<span data-ttu-id="21f81-122">Conectar a la Exchange Server mediante RPC sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="21f81-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="21f81-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="21f81-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="21f81-124">0x2</span><span class="sxs-lookup"><span data-stu-id="21f81-124">0x2</span></span>  <br/> |<span data-ttu-id="21f81-125">Conectar a la Exchange Server usando capa de socket seguro (SSL).</span><span class="sxs-lookup"><span data-stu-id="21f81-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="21f81-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="21f81-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="21f81-127">0x4</span><span class="sxs-lookup"><span data-stu-id="21f81-127">0x4</span></span>  <br/> |<span data-ttu-id="21f81-128">Autenticar mutuamente la sesión al conectarse mediante SSL.</span><span class="sxs-lookup"><span data-stu-id="21f81-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="21f81-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="21f81-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="21f81-130">0x8</span><span class="sxs-lookup"><span data-stu-id="21f81-130">0x8</span></span>  <br/> |<span data-ttu-id="21f81-131">En redes rápidas, conéctese primero con HTTP.</span><span class="sxs-lookup"><span data-stu-id="21f81-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="21f81-132">A continuación, conéctese mediante TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="21f81-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="21f81-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="21f81-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="21f81-134">0x20</span><span class="sxs-lookup"><span data-stu-id="21f81-134">0x20</span></span>  <br/> |<span data-ttu-id="21f81-135">En redes lentas, conéctese primero con HTTP.</span><span class="sxs-lookup"><span data-stu-id="21f81-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="21f81-136">A continuación, conéctese mediante TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="21f81-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="21f81-137">Por ejemplo, para establecer la propiedad **PR_ROH_FLAGS** para activar RPC sobre HTTP, para requerir SSL y para especificar que el protocolo HTTP debe usarse primero en conexiones lentas, establezca el valor de la propiedad PR_ROH_FLAGS en la que es igual **0x23.** `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW`</span><span class="sxs-lookup"><span data-stu-id="21f81-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="21f81-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="21f81-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21f81-139">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="21f81-139">Protocol specifications</span></span>

<span data-ttu-id="21f81-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21f81-140">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21f81-141">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="21f81-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="21f81-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21f81-142">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21f81-143">Define las estructuras de datos básicas que se usan en operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="21f81-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="21f81-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21f81-144">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21f81-145">Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="21f81-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21f81-146">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="21f81-146">Header files</span></span>

<span data-ttu-id="21f81-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21f81-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="21f81-148">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="21f81-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="21f81-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="21f81-149">Mapitags.h</span></span>
  
> <span data-ttu-id="21f81-150">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="21f81-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21f81-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="21f81-151">See also</span></span>



[<span data-ttu-id="21f81-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="21f81-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21f81-153">Propiedades canónicas MAPI</span><span class="sxs-lookup"><span data-stu-id="21f81-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21f81-154">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="21f81-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21f81-155">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="21f81-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

