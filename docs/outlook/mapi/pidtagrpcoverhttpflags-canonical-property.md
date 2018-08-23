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
ms.openlocfilehash: b36f71958528b25829b1ff85b29572b3590f9d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594820"
---
# <a name="pidtagrpcoverhttpflags-canonical-property"></a><span data-ttu-id="1dd1b-103">Propiedad canónica PidTagRpcOverHttpFlags</span><span class="sxs-lookup"><span data-stu-id="1dd1b-103">PidTagRpcOverHttpFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1dd1b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dd1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dd1b-105">Contiene la configuración en un perfil utilizado por Microsoft Office Outlook para conectarse a Microsoft Exchange Server mediante una llamada a procedimiento remoto (RPC) a través del protocolo de transferencia de hipertexto (HTTP).</span><span class="sxs-lookup"><span data-stu-id="1dd1b-105">Contains the settings in a profile used by Microsoft Office Outlook to connect to Microsoft Exchange Server by using a remote procedure call (RPC) over Hypertext Transfer Protocol (HTTP).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1dd1b-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="1dd1b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1dd1b-107">PR_ROH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1dd1b-107">PR_ROH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1dd1b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1dd1b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1dd1b-109">0x6623</span><span class="sxs-lookup"><span data-stu-id="1dd1b-109">0x6623</span></span>  <br/> |
|<span data-ttu-id="1dd1b-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="1dd1b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1dd1b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1dd1b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1dd1b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1dd1b-112">Area:</span></span>  <br/> |<span data-ttu-id="1dd1b-113">Varios</span><span class="sxs-lookup"><span data-stu-id="1dd1b-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dd1b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1dd1b-114">Remarks</span></span>

<span data-ttu-id="1dd1b-115">La propiedad **PR_ROH_FLAGS** se almacena en la sección de perfil Global de un perfil de la interfaz de programación de aplicaciones de mensajería (MAPI).</span><span class="sxs-lookup"><span data-stu-id="1dd1b-115">The **PR_ROH_FLAGS** property is stored in the Global Profile Section of a Messaging Application Programming Interface (MAPI) profile.</span></span> <span data-ttu-id="1dd1b-116">El valor de **PR_ROH_FLAGS** es una máscara de bits que se compone de uno o varios de los siguientes indicadores.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-116">The value of **PR_ROH_FLAGS** is a bitmask that is made up of one or more of the following flags.</span></span> 
  
|<span data-ttu-id="1dd1b-117">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-117">**Name**</span></span>|<span data-ttu-id="1dd1b-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-118">**Value**</span></span>|<span data-ttu-id="1dd1b-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1dd1b-120">**ROHFLAGS_USE_ROH**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-120">**ROHFLAGS_USE_ROH**</span></span> <br/> |<span data-ttu-id="1dd1b-121">0 x 1</span><span class="sxs-lookup"><span data-stu-id="1dd1b-121">0x1</span></span>  <br/> |<span data-ttu-id="1dd1b-122">Conectar con el servidor de Exchange utilizando RPC sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-122">Connect to the Exchange Server using RPC over HTTP.</span></span>  <br/> |
|<span data-ttu-id="1dd1b-123">**ROHFLAGS_SSL_ONLY**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-123">**ROHFLAGS_SSL_ONLY**</span></span> <br/> |<span data-ttu-id="1dd1b-124">0 x 2</span><span class="sxs-lookup"><span data-stu-id="1dd1b-124">0x2</span></span>  <br/> |<span data-ttu-id="1dd1b-125">Conectar con el servidor de Exchange sólo se utiliza capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="1dd1b-125">Connect to the Exchange Server using Secure Socket Layer (SSL) only.</span></span>  <br/> |
|<span data-ttu-id="1dd1b-126">**ROHFLAGS_MUTUAL_AUTH**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-126">**ROHFLAGS_MUTUAL_AUTH**</span></span> <br/> |<span data-ttu-id="1dd1b-127">0 x 4</span><span class="sxs-lookup"><span data-stu-id="1dd1b-127">0x4</span></span>  <br/> |<span data-ttu-id="1dd1b-128">Autenticar mutuamente la sesión al conectar con SSL.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-128">Mutually authenticate the session when connecting by using SSL.</span></span>  <br/> |
|<span data-ttu-id="1dd1b-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-129">**ROHFLAGS_HTTP_FIRST_ON_FAST**</span></span> <br/> |<span data-ttu-id="1dd1b-130">0 x 8</span><span class="sxs-lookup"><span data-stu-id="1dd1b-130">0x8</span></span>  <br/> |<span data-ttu-id="1dd1b-131">En redes rápidas, conectar utilizando HTTP primero.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-131">On fast networks, connect by using HTTP first.</span></span> <span data-ttu-id="1dd1b-132">A continuación, conectar utilizando TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-132">Then, connect by using TCP/IP.</span></span>  <br/> |
|<span data-ttu-id="1dd1b-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span><span class="sxs-lookup"><span data-stu-id="1dd1b-133">**ROHFLAGS_HTTP_FIRST_ON_SLOW**</span></span> <br/> |<span data-ttu-id="1dd1b-134">0 x 20</span><span class="sxs-lookup"><span data-stu-id="1dd1b-134">0x20</span></span>  <br/> |<span data-ttu-id="1dd1b-135">En redes lentas, conectar utilizando HTTP primero.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-135">On slow networks, connect by using HTTP first.</span></span> <span data-ttu-id="1dd1b-136">A continuación, conectar utilizando TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-136">Then, connect by using TCP/IP.</span></span>  <br/> |
   
<span data-ttu-id="1dd1b-137">Por ejemplo, para establecer el **PR_ROH_FLAGS** (propiedad) para activar la RPC a través de HTTP, para requerir SSL y para especificar que se debe usar en primer lugar el protocolo HTTP en conexiones lentas, establezca el valor de la propiedad **PR_ROH_FLAGS** en `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` que es igual a 0 x 23.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-137">For example, to set the **PR_ROH_FLAGS** property to turn on RPC over HTTP, to require SSL, and to specify that the HTTP protocol should be used first on slow connections, set the value of the **PR_ROH_FLAGS** property to  `ROHFLAGS_USE_ROH | ROHFLAGS_SSL_ONLY | ROHFLAGS_HTTP_FIRST_ON_SLOW` which is equal to 0x23.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1dd1b-138">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dd1b-138">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1dd1b-139">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="1dd1b-139">Protocol specifications</span></span>

<span data-ttu-id="1dd1b-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dd1b-140">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dd1b-141">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-141">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1dd1b-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dd1b-142">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dd1b-143">Define las estructuras de datos básicos que se usan en las operaciones remotas.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-143">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="1dd1b-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1dd1b-144">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1dd1b-145">Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-145">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1dd1b-146">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="1dd1b-146">Header files</span></span>

<span data-ttu-id="1dd1b-147">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1dd1b-147">Mapidefs.h</span></span>
  
> <span data-ttu-id="1dd1b-148">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-148">Provides data type definitions.</span></span>
    
<span data-ttu-id="1dd1b-149">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1dd1b-149">Mapitags.h</span></span>
  
> <span data-ttu-id="1dd1b-150">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="1dd1b-150">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1dd1b-151">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1dd1b-151">See also</span></span>



[<span data-ttu-id="1dd1b-152">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1dd1b-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1dd1b-153">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="1dd1b-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1dd1b-154">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="1dd1b-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1dd1b-155">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="1dd1b-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

