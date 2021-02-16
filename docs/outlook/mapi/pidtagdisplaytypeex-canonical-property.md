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
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360777"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="07b93-103">Propiedad canónica PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="07b93-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="07b93-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07b93-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07b93-105">Contiene el tipo de una entrada, con respecto a cómo debe mostrarse la entrada en una fila de una tabla para la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="07b93-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07b93-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="07b93-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07b93-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="07b93-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="07b93-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="07b93-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07b93-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="07b93-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="07b93-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="07b93-110">Data type:</span></span>  <br/> |<span data-ttu-id="07b93-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="07b93-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="07b93-112">Área:</span><span class="sxs-lookup"><span data-stu-id="07b93-112">Area:</span></span>  <br/> |<span data-ttu-id="07b93-113">Libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="07b93-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07b93-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="07b93-114">Remarks</span></span>

<span data-ttu-id="07b93-115">Esta propiedad especifica el tipo de una entrada, con respecto a cómo debe mostrarse en la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="07b93-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="07b93-116">Proporciona información adicional que no se puede representar **en PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="07b93-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="07b93-117">Los valores de **PR_DISPLAY_TYPE** y esta propiedad comienzan por "DT_" y se definen en Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="07b93-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="07b93-118">Todos los valores no documentados están reservados para MAPI.</span><span class="sxs-lookup"><span data-stu-id="07b93-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="07b93-119">Las aplicaciones cliente no deben definir valores nuevos y deben estar preparadas para tratar con un valor no documentado.</span><span class="sxs-lookup"><span data-stu-id="07b93-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="07b93-120">Hay algunas macros que pueden ayudar a determinar los atributos de un objeto, como si es local, remoto o controlado por la seguridad.</span><span class="sxs-lookup"><span data-stu-id="07b93-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="07b93-121">Estas macros incluyen:</span><span class="sxs-lookup"><span data-stu-id="07b93-121">These macros include:</span></span> 
  
|<span data-ttu-id="07b93-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="07b93-122">**Macro**</span></span>|<span data-ttu-id="07b93-123">**Valor**</span><span class="sxs-lookup"><span data-stu-id="07b93-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07b93-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="07b93-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="07b93-125">0x80000000)</span><span class="sxs-lookup"><span data-stu-id="07b93-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="07b93-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="07b93-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="07b93-127">0x40000000</span><span class="sxs-lookup"><span data-stu-id="07b93-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="07b93-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="07b93-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="07b93-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="07b93-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="07b93-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="07b93-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="07b93-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="07b93-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="07b93-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="07b93-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="07b93-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="07b93-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="07b93-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="07b93-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="07b93-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="07b93-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="07b93-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="07b93-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="07b93-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="07b93-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="07b93-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="07b93-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="07b93-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="07b93-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="07b93-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="07b93-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="07b93-141">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="07b93-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="07b93-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="07b93-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="07b93-143">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="07b93-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="07b93-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="07b93-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="07b93-145">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="07b93-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="07b93-146">Las siguientes son algunas notas sobre cómo usar estas macros.</span><span class="sxs-lookup"><span data-stu-id="07b93-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="07b93-147">Para comprobar si una entrada es una entrada remota en otro bosque, aplique la macro DTE_IS_REMOTE_VALID al valor de esta propiedad para comprobar si la marca DTE_FLAG_REMOTE_VALID está establecida en la entrada.</span><span class="sxs-lookup"><span data-stu-id="07b93-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="07b93-148">Si se trata de una entrada remota, puede averiguar el tipo de la entrada remota mediante el uso de la DTE_REMOTE macro.</span><span class="sxs-lookup"><span data-stu-id="07b93-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="07b93-149">En las configuraciones de bosque único y entre bosques, cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, aplicar el DTE_LOCAL de macro al valor de esta propiedad puede permitir identificar aún más el tipo del objeto como DT_DISTLIST (una lista de distribución) o DT_SEC_DISTLIST (una lista de distribución de seguridad).</span><span class="sxs-lookup"><span data-stu-id="07b93-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="07b93-150">Si aplica la macro DTE_LOCAL al valor de **PR_DISPLAY_TYPE_EX** devuelve el tipo DT_REMOTE_MAILUSER, la entrada es una entrada remota.</span><span class="sxs-lookup"><span data-stu-id="07b93-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="07b93-151">En un solo bosque o en una configuración entre bosques donde la replicación está controlada por una lista de control de acceso (ACL), puede usar la macro DTE_IS_ACL_CAPABLE para determinar si una entrada es una entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="07b93-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="07b93-152">En una configuración entre bosques, **PR_DISPLAY_TYPE** tiene el valor de DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="07b93-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="07b93-153">Aplicar la macro DTE_REMOTE al valor de esta propiedad puede permitir obtener el tipo de la entrada remota.</span><span class="sxs-lookup"><span data-stu-id="07b93-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="07b93-154">Los tipos posibles de entrada remota son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="07b93-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="07b93-155">**Tipo de entrada remota**</span><span class="sxs-lookup"><span data-stu-id="07b93-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="07b93-156">**Valor**</span><span class="sxs-lookup"><span data-stu-id="07b93-156">**Value**</span></span>|<span data-ttu-id="07b93-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07b93-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="07b93-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="07b93-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="07b93-159">((ULONG) 0x00000003)</span><span class="sxs-lookup"><span data-stu-id="07b93-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="07b93-160">Lista de distribución dinámica.</span><span class="sxs-lookup"><span data-stu-id="07b93-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="07b93-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="07b93-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="07b93-162">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="07b93-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="07b93-163">Lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="07b93-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="07b93-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="07b93-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="07b93-165">((ULONG) 0x00000008)</span><span class="sxs-lookup"><span data-stu-id="07b93-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="07b93-166">Equipamiento, por ejemplo, una impresora o un proyector.</span><span class="sxs-lookup"><span data-stu-id="07b93-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="07b93-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="07b93-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="07b93-168">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="07b93-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="07b93-169">Usuario con un buzón.</span><span class="sxs-lookup"><span data-stu-id="07b93-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="07b93-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="07b93-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="07b93-171">((ULONG) 0x00000000)</span><span class="sxs-lookup"><span data-stu-id="07b93-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="07b93-172">Una entrada de lista de direcciones en la lista global de direcciones.</span><span class="sxs-lookup"><span data-stu-id="07b93-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="07b93-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="07b93-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="07b93-174">((ULONG) 0x00000007)</span><span class="sxs-lookup"><span data-stu-id="07b93-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="07b93-175">Sala de conferencias.</span><span class="sxs-lookup"><span data-stu-id="07b93-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="07b93-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="07b93-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="07b93-177">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="07b93-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="07b93-178">Lista de distribución de seguridad.</span><span class="sxs-lookup"><span data-stu-id="07b93-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="07b93-179">Tanto en un bosque único como en una configuración entre bosques, cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, aplicar la macro DTE_LOCAL al valor de esta propiedad puede permitir obtener el tipo de la lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="07b93-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="07b93-180">Los tipos posibles de lista de distribución son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="07b93-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="07b93-181">**Tipo de lista de distribución**</span><span class="sxs-lookup"><span data-stu-id="07b93-181">**Type of Distribution List**</span></span>|<span data-ttu-id="07b93-182">**Valor**</span><span class="sxs-lookup"><span data-stu-id="07b93-182">**Value**</span></span>|<span data-ttu-id="07b93-183">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07b93-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="07b93-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="07b93-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="07b93-185">((ULONG) 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="07b93-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="07b93-186">Lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="07b93-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="07b93-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="07b93-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="07b93-188">((ULONG) 0x00000009)</span><span class="sxs-lookup"><span data-stu-id="07b93-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="07b93-189">Lista de distribución de seguridad.</span><span class="sxs-lookup"><span data-stu-id="07b93-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="07b93-190">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="07b93-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="07b93-191">Especificaciones del protocolo</span><span class="sxs-lookup"><span data-stu-id="07b93-191">Protocol specifications</span></span>

<span data-ttu-id="07b93-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07b93-192">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07b93-193">Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.</span><span class="sxs-lookup"><span data-stu-id="07b93-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="07b93-194">[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="07b93-194">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="07b93-195">Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.</span><span class="sxs-lookup"><span data-stu-id="07b93-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="07b93-196">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="07b93-196">Header files</span></span>

<span data-ttu-id="07b93-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07b93-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="07b93-198">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="07b93-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="07b93-199">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="07b93-199">Mapitags.h</span></span>
  
> <span data-ttu-id="07b93-200">Contiene definiciones de propiedades enumeradas como nombres alternativos.</span><span class="sxs-lookup"><span data-stu-id="07b93-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07b93-201">Consulte también</span><span class="sxs-lookup"><span data-stu-id="07b93-201">See also</span></span>



[<span data-ttu-id="07b93-202">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="07b93-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07b93-203">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="07b93-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07b93-204">Asignación de nombres de propiedades canónicas a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="07b93-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07b93-205">Asignación de nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="07b93-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

