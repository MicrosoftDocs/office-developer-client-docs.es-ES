---
title: Propiedad canónica PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 30482f7d6acef7377a1b63bc3de4e43be48d8608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583361"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="60569-103">Propiedad canónica PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="60569-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="60569-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60569-105">Contiene el tipo de una entrada, con respecto a cómo se debe mostrar la entrada de una fila en una tabla de la lista Global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="60569-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="60569-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="60569-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="60569-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="60569-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="60569-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="60569-108">Identifier:</span></span>  <br/> |<span data-ttu-id="60569-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="60569-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="60569-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="60569-110">Data type:</span></span>  <br/> |<span data-ttu-id="60569-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="60569-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="60569-112">Área:</span><span class="sxs-lookup"><span data-stu-id="60569-112">Area:</span></span>  <br/> |<span data-ttu-id="60569-113">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="60569-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60569-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60569-114">Remarks</span></span>

<span data-ttu-id="60569-115">Esta propiedad especifica el tipo de una entrada, con respecto a determinar cómo deben mostrarse en la lista Global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="60569-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="60569-116">Se proporciona información adicional que no se pueden representar en **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="60569-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="60569-117">Los valores de **PR_DISPLAY_TYPE** y esta propiedad comienzan con "DT_" y se definen en Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="60569-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="60569-118">Todos los valores no documentados están reservados para MAPI.</span><span class="sxs-lookup"><span data-stu-id="60569-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="60569-119">Las aplicaciones cliente no deben definir los nuevos valores y deben estar preparadas abordar los problemas con un valor sin documentar.</span><span class="sxs-lookup"><span data-stu-id="60569-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="60569-120">Hay algunas macros que pueden ayudar a determinar los atributos de un objeto como si es local, remoto o con control de seguridad.</span><span class="sxs-lookup"><span data-stu-id="60569-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="60569-121">Estas macros se incluyen:</span><span class="sxs-lookup"><span data-stu-id="60569-121">These macros include:</span></span> 
  
|<span data-ttu-id="60569-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="60569-122">**Macro**</span></span>|<span data-ttu-id="60569-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="60569-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60569-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="60569-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="60569-125">0 x 80000000)</span><span class="sxs-lookup"><span data-stu-id="60569-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="60569-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="60569-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="60569-127">0 x 40000000</span><span class="sxs-lookup"><span data-stu-id="60569-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="60569-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="60569-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="60569-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="60569-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="60569-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="60569-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="60569-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="60569-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="60569-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="60569-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="60569-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="60569-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="60569-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="60569-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="60569-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="60569-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="60569-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="60569-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="60569-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="60569-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="60569-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="60569-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="60569-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="60569-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="60569-140">POR EJEMPLO</span><span class="sxs-lookup"><span data-stu-id="60569-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="60569-141">((ULONG) 0 X 00000007)</span><span class="sxs-lookup"><span data-stu-id="60569-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="60569-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="60569-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="60569-143">((ULONG) 0 X 00000008)</span><span class="sxs-lookup"><span data-stu-id="60569-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="60569-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="60569-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="60569-145">((ULONG) 0 X 00000009)</span><span class="sxs-lookup"><span data-stu-id="60569-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="60569-146">Las siguientes son algunas notas sobre cómo usar estas macros.</span><span class="sxs-lookup"><span data-stu-id="60569-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="60569-147">Para comprobar si una entrada es una entrada remota en otro bosque, se aplican la macro DTE_IS_REMOTE_VALID para el valor de esta propiedad para comprobar si se ha establecido el indicador DTE_FLAG_REMOTE_VALID en la entrada.</span><span class="sxs-lookup"><span data-stu-id="60569-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="60569-148">Si es una entrada de remota, a continuación, puede encontrar el tipo de la entrada de remota mediante el uso de la macro DTE_REMOTE.</span><span class="sxs-lookup"><span data-stu-id="60569-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="60569-149">En las configuraciones de un solo bosque y entre bosques, cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, la aplicación de la macro DTE_LOCAL para el valor de esta propiedad puede dejar que aún más identificar el tipo del objeto como o bien DT_DISTLIST (una lista de distribución) o DT_SEC_DISTLIST (una lista de distribución de seguridad).</span><span class="sxs-lookup"><span data-stu-id="60569-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="60569-150">Si aplica la macro DTE_LOCAL para el valor de **PR_DISPLAY_TYPE_EX** y devuelve el tipo DT_REMOTE_MAILUSER, a continuación, el movimiento es un movimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="60569-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="60569-151">En un solo bosque o en una configuración entre bosques donde replicación está controlada por una lista de Control de acceso (ACL), puede usar la macro DTE_IS_ACL_CAPABLE para determinar si una entrada es una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="60569-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="60569-152">En una configuración entre bosques, **PR_DISPLAY_TYPE** tiene el valor de DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="60569-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="60569-153">Aplicar la macro DTE_REMOTE para el valor de esta propiedad puede dejar que obtener el tipo de la entrada remoto.</span><span class="sxs-lookup"><span data-stu-id="60569-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="60569-154">Los posibles tipos de entrada remoto son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="60569-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="60569-155">**Tipo de movimiento remoto**</span><span class="sxs-lookup"><span data-stu-id="60569-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="60569-156">**Valor**</span><span class="sxs-lookup"><span data-stu-id="60569-156">**Value**</span></span>|<span data-ttu-id="60569-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60569-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="60569-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="60569-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="60569-159">((ULONG) 0 X 00000003)</span><span class="sxs-lookup"><span data-stu-id="60569-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="60569-160">Lista de distribución dinámica.</span><span class="sxs-lookup"><span data-stu-id="60569-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="60569-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="60569-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="60569-162">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="60569-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="60569-163">Lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="60569-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="60569-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="60569-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="60569-165">((ULONG) 0 X 00000008)</span><span class="sxs-lookup"><span data-stu-id="60569-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="60569-166">Equipamiento, por ejemplo, una impresora o a proyectores.</span><span class="sxs-lookup"><span data-stu-id="60569-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="60569-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="60569-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="60569-168">((ULONG) 0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="60569-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="60569-169">Usuario con un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="60569-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="60569-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="60569-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="60569-171">((ULONG) 0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="60569-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="60569-172">Una entrada de la lista de direcciones en la lista Global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="60569-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="60569-173">POR EJEMPLO</span><span class="sxs-lookup"><span data-stu-id="60569-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="60569-174">((ULONG) 0 X 00000007)</span><span class="sxs-lookup"><span data-stu-id="60569-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="60569-175">Sala de conferencias.</span><span class="sxs-lookup"><span data-stu-id="60569-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="60569-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="60569-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="60569-177">((ULONG) 0 X 00000009)</span><span class="sxs-lookup"><span data-stu-id="60569-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="60569-178">Lista de distribución de seguridad.</span><span class="sxs-lookup"><span data-stu-id="60569-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="60569-179">En un solo bosque y en entre bosques configuración cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, la aplicación de la macro DTE_LOCAL para el valor de esta propiedad puede dejar que obtener el tipo de la lista de distribución .</span><span class="sxs-lookup"><span data-stu-id="60569-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="60569-180">Los posibles tipos de lista de distribución son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="60569-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="60569-181">**Tipo de lista de distribución**</span><span class="sxs-lookup"><span data-stu-id="60569-181">**Type of Distribution List**</span></span>|<span data-ttu-id="60569-182">**Valor**</span><span class="sxs-lookup"><span data-stu-id="60569-182">**Value**</span></span>|<span data-ttu-id="60569-183">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="60569-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="60569-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="60569-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="60569-185">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="60569-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="60569-186">Lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="60569-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="60569-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="60569-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="60569-188">((ULONG) 0 X 00000009)</span><span class="sxs-lookup"><span data-stu-id="60569-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="60569-189">Lista de distribución de seguridad.</span><span class="sxs-lookup"><span data-stu-id="60569-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="60569-190">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="60569-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="60569-191">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="60569-191">Protocol specifications</span></span>

<span data-ttu-id="60569-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60569-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60569-193">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="60569-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="60569-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60569-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60569-195">Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="60569-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="60569-196">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="60569-196">Header files</span></span>

<span data-ttu-id="60569-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60569-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="60569-198">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="60569-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="60569-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="60569-199">Mapitags.h</span></span>
  
> <span data-ttu-id="60569-200">Contiene las definiciones de las propiedades que aparecen como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="60569-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60569-201">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="60569-201">See also</span></span>



[<span data-ttu-id="60569-202">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="60569-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="60569-203">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="60569-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="60569-204">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="60569-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="60569-205">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="60569-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

