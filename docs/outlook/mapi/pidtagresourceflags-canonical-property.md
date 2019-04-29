---
title: Propiedad canónica PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436233"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="5b6a8-103">Propiedad canónica PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="5b6a8-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="5b6a8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b6a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b6a8-105">Contiene una máscara de máscara de marcas para servicios de mensajes y proveedores.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b6a8-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5b6a8-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5b6a8-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="5b6a8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5b6a8-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="5b6a8-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="5b6a8-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="5b6a8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5b6a8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5b6a8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-112">Area:</span></span>  <br/> |<span data-ttu-id="5b6a8-113">Common MAPI</span><span class="sxs-lookup"><span data-stu-id="5b6a8-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b6a8-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5b6a8-114">Remarks</span></span>

<span data-ttu-id="5b6a8-115">Esta propiedad describe las características de un servicio de mensajes, un proveedor de servicios o un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="5b6a8-116">Las marcas que se establecen para esta propiedad dependen de su contexto.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="5b6a8-117">Por ejemplo, algunas marcas solo son válidas para los objetos de estado y otros indicadores sólo para las columnas de la tabla de servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="5b6a8-118">Las marcas son de tres clases: Static, modificable y Dynamic.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="5b6a8-119">MAPI establece las marcas estáticas a partir de los datos de MAPISVC. INF y nunca se modificó.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="5b6a8-120">MAPI establece las marcas modificables desde MAPISVC. INF, pero puede cambiarse posteriormente.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="5b6a8-121">Los métodos MAPI pueden establecer y restablecer marcas dinámicas.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="5b6a8-122">Para un servicio de mensajes, se pueden establecer uno o varios de los siguientes indicadores en esta propiedad:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="5b6a8-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-124">Reserved.</span></span> <span data-ttu-id="5b6a8-125">No usar.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-125">Do not use.</span></span>
    
<span data-ttu-id="5b6a8-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-127">Forma.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-127">Dynamic.</span></span> <span data-ttu-id="5b6a8-128">El servicio de mensajes contiene el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-128">The message service contains the default store.</span></span> <span data-ttu-id="5b6a8-129">Se debe mostrar una interfaz de usuario para pedir confirmación al usuario antes de eliminar o mover este servicio del perfil.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="5b6a8-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="5b6a8-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="5b6a8-131">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-131">Static.</span></span> <span data-ttu-id="5b6a8-132">El marcador de nivel de servicio que se debe establecer para indicar que ninguno de los proveedores del servicio de mensajes se puede usar para proporcionar una identidad.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="5b6a8-133">Se debe establecer esta marca o SERVICE_PRIMARY_IDENTITY, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="5b6a8-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="5b6a8-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="5b6a8-135">Modificable.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-135">Modifiable.</span></span> <span data-ttu-id="5b6a8-136">El servicio de mensajes correspondiente contiene el proveedor usado para la identidad principal de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="5b6a8-137">Use [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="5b6a8-138">Se debe establecer esta marca o SERVICE_NO_PRIMARY_IDENTITY, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="5b6a8-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="5b6a8-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="5b6a8-140">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-140">Static.</span></span> <span data-ttu-id="5b6a8-141">Cualquier intento de crear o copiar este servicio de mensajes en un perfil en el que el servicio ya existe producirá un error.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="5b6a8-142">Para crear un servicio de mensaje de copia único, agregue la propiedad **PR_RESOURCE_FLAGS** a la sección del servicio en MAPISVC. INF y establece esta marca.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="5b6a8-143">Para un proveedor de servicios, se pueden establecer uno o varios de los siguientes indicadores en **PR_RESOURCE_FLAGS**:</span><span class="sxs-lookup"><span data-stu-id="5b6a8-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="5b6a8-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="5b6a8-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="5b6a8-145">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-145">Static.</span></span> <span data-ttu-id="5b6a8-146">El enlace de la cola de impresión debe procesar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="5b6a8-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="5b6a8-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="5b6a8-148">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-148">Static.</span></span> <span data-ttu-id="5b6a8-149">El enlace de la cola de impresión debe procesar los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="5b6a8-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="5b6a8-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="5b6a8-151">Modificable.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-151">Modifiable.</span></span> <span data-ttu-id="5b6a8-152">Esta identidad debe aplicarse a los mensajes salientes si el perfil contiene varias instancias de este proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="5b6a8-153">Esto puede ocurrir si varias instancias de un único proveedor de transporte aparecen en el perfil.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="5b6a8-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-155">Modificable.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-155">Modifiable.</span></span> <span data-ttu-id="5b6a8-156">Este almacén de mensajes es el almacén predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="5b6a8-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="5b6a8-158">Forma.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-158">Dynamic.</span></span> <span data-ttu-id="5b6a8-159">Las carpetas estándar de este almacén de mensajes, incluida la carpeta raíz del mensaje interpersonal (IPM), todavía no se han comprobado.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="5b6a8-160">MAPI establece y borra esta marca.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="5b6a8-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-162">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-162">Static.</span></span> <span data-ttu-id="5b6a8-163">Este almacén de mensajes no puede convertirse en el almacén de mensajes predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="5b6a8-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="5b6a8-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="5b6a8-165">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-165">Static.</span></span> <span data-ttu-id="5b6a8-166">Este proveedor no proporciona una identidad en su fila de estado.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="5b6a8-167">Se debe establecer esta marca o STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="5b6a8-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-169">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-169">Static.</span></span> <span data-ttu-id="5b6a8-170">Este proveedor de transporte está estrechamente acoplado a un almacén de mensajes y proporciona la propiedad **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) en su fila de estado.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="5b6a8-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="5b6a8-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="5b6a8-172">Modificable.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-172">Modifiable.</span></span> <span data-ttu-id="5b6a8-173">Este proveedor suministra la identidad principal para la sesión; el identificador de entrada para el objeto que suministra la identidad se devuelve desde [IMAPISession:: QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="5b6a8-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="5b6a8-174">Se debe establecer esta marca o **STATUS_NO_PRIMARY_IDENTITY** .</span><span class="sxs-lookup"><span data-stu-id="5b6a8-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="5b6a8-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-176">Modificable.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-176">Modifiable.</span></span> <span data-ttu-id="5b6a8-177">Este almacén de mensajes se debe usar cuando una aplicación cliente inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="5b6a8-178">Una vez abierto, este almacén debe establecerse como el almacén predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="5b6a8-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-180">Modificable.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-180">Modifiable.</span></span> <span data-ttu-id="5b6a8-181">Este almacén de mensajes debe usarse si el almacén principal no está disponible cuando una aplicación cliente inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="5b6a8-182">Una vez abierto, este almacén debe establecerse como el almacén predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="5b6a8-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="5b6a8-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="5b6a8-184">Forma.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-184">Dynamic.</span></span> <span data-ttu-id="5b6a8-185">Simple MAPI usará este almacén de mensajes como almacén de mensajes predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="5b6a8-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="5b6a8-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="5b6a8-187">Forma.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-187">Dynamic.</span></span> <span data-ttu-id="5b6a8-188">Este almacén de mensajes no debe publicarse en la tabla de almacén de mensajes y se eliminará del perfil tras el cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="5b6a8-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="5b6a8-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="5b6a8-190">Static.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-190">Static.</span></span> <span data-ttu-id="5b6a8-191">Este transporte espera ser el último transporte seleccionado para enviar un mensaje cuando varios proveedores de transporte puedan transmitir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="5b6a8-192">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b6a8-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5b6a8-193">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="5b6a8-193">Header files</span></span>

<span data-ttu-id="5b6a8-194">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5b6a8-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="5b6a8-195">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="5b6a8-196">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5b6a8-196">Mapitags.h</span></span>
  
> <span data-ttu-id="5b6a8-197">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="5b6a8-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b6a8-198">Ver también</span><span class="sxs-lookup"><span data-stu-id="5b6a8-198">See also</span></span>



[<span data-ttu-id="5b6a8-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="5b6a8-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="5b6a8-200">Propiedad canónica PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="5b6a8-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="5b6a8-201">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="5b6a8-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5b6a8-202">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="5b6a8-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5b6a8-203">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="5b6a8-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5b6a8-204">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="5b6a8-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

