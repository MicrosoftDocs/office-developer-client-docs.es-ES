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
ms.openlocfilehash: 875b37183134a6c5beca76ab7910cf601d1b6175
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567506"
---
# <a name="pidtagresourceflags-canonical-property"></a><span data-ttu-id="d2659-103">Propiedad canónica PidTagResourceFlags</span><span class="sxs-lookup"><span data-stu-id="d2659-103">PidTagResourceFlags Canonical Property</span></span>

  
  
<span data-ttu-id="d2659-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2659-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2659-105">Contiene una máscara de bits de indicadores para servicios de mensajes y proveedores.</span><span class="sxs-lookup"><span data-stu-id="d2659-105">Contains a bitmask of flags for message services and providers.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2659-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d2659-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d2659-107">PR_RESOURCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d2659-107">PR_RESOURCE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="d2659-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d2659-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d2659-109">0x3009</span><span class="sxs-lookup"><span data-stu-id="d2659-109">0x3009</span></span>  <br/> |
|<span data-ttu-id="d2659-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d2659-110">Data type:</span></span>  <br/> |<span data-ttu-id="d2659-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d2659-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d2659-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d2659-112">Area:</span></span>  <br/> |<span data-ttu-id="d2659-113">MAPI comunes</span><span class="sxs-lookup"><span data-stu-id="d2659-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2659-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2659-114">Remarks</span></span>

<span data-ttu-id="d2659-115">Esta propiedad describe las características de un servicio de mensajes, un proveedor de servicios o un objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="d2659-115">This property describes the characteristics of a message service, a service provider, or a status object.</span></span> <span data-ttu-id="d2659-116">Los indicadores que se han establecido para esta propiedad dependen de su contexto.</span><span class="sxs-lookup"><span data-stu-id="d2659-116">The flags that are set for this property depend on its context.</span></span> <span data-ttu-id="d2659-117">Por ejemplo, algunas marcas son válidos únicamente para los objetos de estado y otros marcadores sólo para las columnas en la tabla de servicios de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d2659-117">For example, some flags are valid only for status objects and other flags only for columns in the message service table.</span></span> 
  
<span data-ttu-id="d2659-118">Los marcadores son de tres clases: estáticos, modificable y dinámicos.</span><span class="sxs-lookup"><span data-stu-id="d2659-118">The flags are of three classes: static, modifiable, and dynamic.</span></span> <span data-ttu-id="d2659-119">Se establecen indicadores estáticas por MAPI desde los datos en MAPISVC. INF y nunca se modifica.</span><span class="sxs-lookup"><span data-stu-id="d2659-119">Static flags are set by MAPI from data in MAPISVC.INF and never altered.</span></span> <span data-ttu-id="d2659-120">Se establecen indicadores modificables por MAPI desde MAPISVC. INF pero se puede cambiar posteriormente.</span><span class="sxs-lookup"><span data-stu-id="d2659-120">Modifiable flags are set by MAPI from MAPISVC.INF but can be subsequently changed.</span></span> <span data-ttu-id="d2659-121">Marcas dinámicos se pueden establecer y restablecer por métodos MAPI.</span><span class="sxs-lookup"><span data-stu-id="d2659-121">Dynamic flags can be set and reset by MAPI methods.</span></span>
  
<span data-ttu-id="d2659-122">Para un servicio de mensajes, se pueden establecer en esta propiedad uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d2659-122">For a message service, one or more of the following flags can be set in this property:</span></span>
  
<span data-ttu-id="d2659-123">SERVICE_CREATE_WITH_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-123">SERVICE_CREATE_WITH_STORE</span></span> 
  
> <span data-ttu-id="d2659-124">Reservado.</span><span class="sxs-lookup"><span data-stu-id="d2659-124">Reserved.</span></span> <span data-ttu-id="d2659-125">No la use.</span><span class="sxs-lookup"><span data-stu-id="d2659-125">Do not use.</span></span>
    
<span data-ttu-id="d2659-126">SERVICE_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-126">SERVICE_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="d2659-127">Dinámico.</span><span class="sxs-lookup"><span data-stu-id="d2659-127">Dynamic.</span></span> <span data-ttu-id="d2659-128">El servicio de mensajes contiene el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d2659-128">The message service contains the default store.</span></span> <span data-ttu-id="d2659-129">Una interfaz de usuario debe mostrarse preguntar al usuario la confirmación antes de eliminar o mover este servicio fuera de los perfiles.</span><span class="sxs-lookup"><span data-stu-id="d2659-129">A user interface should be displayed prompting the user for confirmation before deleting or moving this service out of the profile.</span></span> 
    
<span data-ttu-id="d2659-130">SERVICE_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d2659-130">SERVICE_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d2659-131">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-131">Static.</span></span> <span data-ttu-id="d2659-132">El indicador de nivel de servicio que se debe establecer para indicar que ninguno de los proveedores en el servicio de mensajes se puede usar para proporcionar una identidad.</span><span class="sxs-lookup"><span data-stu-id="d2659-132">The service level flag that should be set to indicate that none of the providers in the message service can be used to supply an identity.</span></span> <span data-ttu-id="d2659-133">Este indicador o el SERVICE_PRIMARY_IDENTITY debe ser set, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="d2659-133">Either this flag or SERVICE_PRIMARY_IDENTITY should be set, but not both.</span></span>
    
<span data-ttu-id="d2659-134">SERVICE_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d2659-134">SERVICE_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d2659-135">Puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d2659-135">Modifiable.</span></span> <span data-ttu-id="d2659-136">El servicio de mensajes correspondiente contiene el proveedor que se utiliza para la identidad principal de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="d2659-136">The corresponding message service contains the provider used for the primary identity for this session.</span></span> <span data-ttu-id="d2659-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="d2659-137">Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) to set this flag.</span></span> <span data-ttu-id="d2659-138">Este indicador o el SERVICE_NO_PRIMARY_IDENTITY debe ser set, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="d2659-138">Either this flag or SERVICE_NO_PRIMARY_IDENTITY should be set, but not both.</span></span> 
    
<span data-ttu-id="d2659-139">SERVICE_SINGLE_COPY</span><span class="sxs-lookup"><span data-stu-id="d2659-139">SERVICE_SINGLE_COPY</span></span> 
  
> <span data-ttu-id="d2659-140">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-140">Static.</span></span> <span data-ttu-id="d2659-141">Se producirá un error en cualquier intento para crear o copiar este servicio de mensajes a un perfil de ubicación donde ya existe el servicio.</span><span class="sxs-lookup"><span data-stu-id="d2659-141">Any attempt to create or copy this message service into a profile where the service already exists will fail.</span></span> <span data-ttu-id="d2659-142">Para crear una copia de un solo servicio de mensajes agregar la propiedad **PR_RESOURCE_FLAGS** a la sección del servicio MAPISVC. INF y establezca esta marca.</span><span class="sxs-lookup"><span data-stu-id="d2659-142">To create a single copy message service add the **PR_RESOURCE_FLAGS** property to the service's section in MAPISVC.INF and set this flag.</span></span> 
    
<span data-ttu-id="d2659-143">Para un proveedor de servicios, se pueden establecer en **PR_RESOURCE_FLAGS**uno o varios de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="d2659-143">For a service provider, one or more of the following flags can be set in **PR_RESOURCE_FLAGS**:</span></span>
  
<span data-ttu-id="d2659-144">HOOK_INBOUND</span><span class="sxs-lookup"><span data-stu-id="d2659-144">HOOK_INBOUND</span></span> 
  
> <span data-ttu-id="d2659-145">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-145">Static.</span></span> <span data-ttu-id="d2659-146">El enlace de la cola de impresión debe procesar los mensajes entrantes.</span><span class="sxs-lookup"><span data-stu-id="d2659-146">The spooler hook needs to process inbound messages.</span></span>
    
<span data-ttu-id="d2659-147">HOOK_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="d2659-147">HOOK_OUTBOUND</span></span> 
  
> <span data-ttu-id="d2659-148">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-148">Static.</span></span> <span data-ttu-id="d2659-149">El enlace de la cola de impresión necesita para procesar los mensajes salientes.</span><span class="sxs-lookup"><span data-stu-id="d2659-149">The spooler hook needs to process outbound messages.</span></span> 
    
<span data-ttu-id="d2659-150">STATUS_DEFAULT_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="d2659-150">STATUS_DEFAULT_OUTBOUND</span></span> 
  
> <span data-ttu-id="d2659-151">Puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d2659-151">Modifiable.</span></span> <span data-ttu-id="d2659-152">Esta identidad debe aplicarse a los mensajes salientes si el perfil contiene varias instancias de este proveedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="d2659-152">This identity should be applied to outbound messages if the profile contains multiple instances of this transport provider.</span></span> <span data-ttu-id="d2659-153">Esto puede ocurrir si varias instancias de un proveedor de transporte único aparecen en el perfil.</span><span class="sxs-lookup"><span data-stu-id="d2659-153">This can happen if multiple instances of a single transport provider appear in the profile.</span></span>
    
<span data-ttu-id="d2659-154">STATUS_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-154">STATUS_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="d2659-155">Puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d2659-155">Modifiable.</span></span> <span data-ttu-id="d2659-156">Este almacén de mensajes es el almacén predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="d2659-156">This message store is the default store for the profile.</span></span> 
    
<span data-ttu-id="d2659-157">STATUS_NEED_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="d2659-157">STATUS_NEED_IPM_TREE</span></span> 
  
> <span data-ttu-id="d2659-158">Dinámico.</span><span class="sxs-lookup"><span data-stu-id="d2659-158">Dynamic.</span></span> <span data-ttu-id="d2659-159">Aún no se ha comprobado las carpetas estándar en este almacén de mensajes, incluyendo la carpeta raíz de mensajes interpersonales (IPM).</span><span class="sxs-lookup"><span data-stu-id="d2659-159">The standard folders in this message store, including the interpersonal message (IPM) root folder, have not yet been verified.</span></span> <span data-ttu-id="d2659-160">MAPI establece y borra este indicador.</span><span class="sxs-lookup"><span data-stu-id="d2659-160">MAPI sets and clears this flag.</span></span> 
    
<span data-ttu-id="d2659-161">STATUS_NO_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-161">STATUS_NO_DEFAULT_STORE</span></span> 
  
> <span data-ttu-id="d2659-162">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-162">Static.</span></span> <span data-ttu-id="d2659-163">Este almacén de mensajes es capaz de convertirse en el almacén de mensajes predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="d2659-163">This message store is incapable of becoming the default message store for the profile.</span></span>
    
<span data-ttu-id="d2659-164">STATUS_NO_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d2659-164">STATUS_NO_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d2659-165">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-165">Static.</span></span> <span data-ttu-id="d2659-166">Este proveedor no proporcionar una identidad en su fila de estado.</span><span class="sxs-lookup"><span data-stu-id="d2659-166">This provider does not furnish an identity in its status row.</span></span> <span data-ttu-id="d2659-167">Se debe establecer este indicador o STATUS_PRIMARY_IDENTITY.</span><span class="sxs-lookup"><span data-stu-id="d2659-167">Either this flag or STATUS_PRIMARY_IDENTITY must be set.</span></span>
    
<span data-ttu-id="d2659-168">STATUS_OWN_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-168">STATUS_OWN_STORE</span></span> 
  
> <span data-ttu-id="d2659-169">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-169">Static.</span></span> <span data-ttu-id="d2659-170">Este proveedor de transporte se complementa con un almacén de mensajes y proporciona la propiedad **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) en la fila de estado correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d2659-170">This transport provider is tightly coupled with a message store and furnishes the **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) property in its status row.</span></span>
    
<span data-ttu-id="d2659-171">STATUS_PRIMARY_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="d2659-171">STATUS_PRIMARY_IDENTITY</span></span> 
  
> <span data-ttu-id="d2659-172">Puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d2659-172">Modifiable.</span></span> <span data-ttu-id="d2659-173">Este proveedor aporta la identidad principal para la sesión; se devuelve el identificador de entrada para el objeto de suministro de la identidad de [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span><span class="sxs-lookup"><span data-stu-id="d2659-173">This provider furnishes the primary identity for the session; the entry identifier for the object furnishing the identity is returned from [IMAPISession::QueryIdentity](imapisession-queryidentity.md).</span></span> <span data-ttu-id="d2659-174">Se debe establecer este indicador o **STATUS_NO_PRIMARY_IDENTITY** .</span><span class="sxs-lookup"><span data-stu-id="d2659-174">Either this flag or **STATUS_NO_PRIMARY_IDENTITY** must be set.</span></span> 
    
<span data-ttu-id="d2659-175">STATUS_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-175">STATUS_PRIMARY_STORE</span></span> 
  
> <span data-ttu-id="d2659-176">Puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d2659-176">Modifiable.</span></span> <span data-ttu-id="d2659-177">Este almacén de mensajes es para usarse cuando una aplicación cliente inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="d2659-177">This message store is to be used when a client application logs on.</span></span> <span data-ttu-id="d2659-178">Una vez abierto, se debe establecer este almacén como el almacén predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="d2659-178">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="d2659-179">STATUS_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-179">STATUS_SECONDARY_STORE</span></span> 
  
> <span data-ttu-id="d2659-180">Puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d2659-180">Modifiable.</span></span> <span data-ttu-id="d2659-181">Este almacén de mensajes es que se usará si el almacén principal no está disponible cuando una aplicación cliente inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="d2659-181">This message store is to be used if the primary store is not available when a client application logs on.</span></span> <span data-ttu-id="d2659-182">Una vez abierto, se debe establecer este almacén como el almacén predeterminado para el perfil.</span><span class="sxs-lookup"><span data-stu-id="d2659-182">Once opened, this store should be set as the default store for the profile.</span></span> 
    
<span data-ttu-id="d2659-183">STATUS_SIMPLE_STORE</span><span class="sxs-lookup"><span data-stu-id="d2659-183">STATUS_SIMPLE_STORE</span></span> 
  
> <span data-ttu-id="d2659-184">Dinámico.</span><span class="sxs-lookup"><span data-stu-id="d2659-184">Dynamic.</span></span> <span data-ttu-id="d2659-185">Como su almacén de mensajes de forma predeterminada, se usará este almacén de mensajes mediante Simple MAPI.</span><span class="sxs-lookup"><span data-stu-id="d2659-185">This message store will be used by Simple MAPI as its default message store.</span></span>
    
<span data-ttu-id="d2659-186">STATUS_TEMP_SECTION</span><span class="sxs-lookup"><span data-stu-id="d2659-186">STATUS_TEMP_SECTION</span></span> 
  
> <span data-ttu-id="d2659-187">Dinámico.</span><span class="sxs-lookup"><span data-stu-id="d2659-187">Dynamic.</span></span> <span data-ttu-id="d2659-188">Este almacén de mensajes no se debe publicar en la tabla de almacén de mensajes y se eliminarán del perfil de después de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="d2659-188">This message store should not be published in the message store table and will be deleted from the profile after logoff.</span></span> 
    
<span data-ttu-id="d2659-189">STATUS_XP_PREFER_LAST</span><span class="sxs-lookup"><span data-stu-id="d2659-189">STATUS_XP_PREFER_LAST</span></span> 
  
> <span data-ttu-id="d2659-190">Static.</span><span class="sxs-lookup"><span data-stu-id="d2659-190">Static.</span></span> <span data-ttu-id="d2659-191">Este transporte espera que sea la última transporte seleccionado para enviar un mensaje cuando varios proveedores de transporte se pueden transmitir el mensaje.</span><span class="sxs-lookup"><span data-stu-id="d2659-191">This transport expects to be the last transport selected to send a message when multiple transport providers are able to transmit the message.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d2659-192">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2659-192">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d2659-193">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d2659-193">Header files</span></span>

<span data-ttu-id="d2659-194">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d2659-194">Mapidefs.h</span></span>
  
> <span data-ttu-id="d2659-195">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d2659-195">Provides data type definitions.</span></span>
    
<span data-ttu-id="d2659-196">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d2659-196">Mapitags.h</span></span>
  
> <span data-ttu-id="d2659-197">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="d2659-197">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d2659-198">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d2659-198">See also</span></span>



[<span data-ttu-id="d2659-199">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="d2659-199">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="d2659-200">Propiedad canónica PidTagIdentityEntryId</span><span class="sxs-lookup"><span data-stu-id="d2659-200">PidTagIdentityEntryId Canonical Property</span></span>](pidtagidentityentryid-canonical-property.md)


[<span data-ttu-id="d2659-201">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d2659-201">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d2659-202">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d2659-202">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d2659-203">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d2659-203">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d2659-204">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d2659-204">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

