---
title: Propiedad canónica PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342697"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="81efe-103">Propiedad canónica PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="81efe-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="81efe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81efe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81efe-105">Contiene un conjunto de bits que indica los derechos de este miembro en una carpeta o buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="81efe-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="81efe-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="81efe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81efe-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="81efe-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="81efe-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="81efe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81efe-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="81efe-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="81efe-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="81efe-110">Data type:</span></span>  <br/> |<span data-ttu-id="81efe-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="81efe-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="81efe-112">Área:</span><span class="sxs-lookup"><span data-stu-id="81efe-112">Area:</span></span>  <br/> |<span data-ttu-id="81efe-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="81efe-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81efe-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="81efe-114">Remarks</span></span>

<span data-ttu-id="81efe-115">Esta propiedad se usa en la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para definir los derechos de un miembro en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="81efe-116">Estos derechos se pueden mostrar y modificar.</span><span class="sxs-lookup"><span data-stu-id="81efe-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="81efe-117">Los siguientes valores son derechos definidos para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="81efe-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="81efe-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="81efe-118">frightsReadAny</span></span>
  
> <span data-ttu-id="81efe-119">El miembro puede leer los mensajes.</span><span class="sxs-lookup"><span data-stu-id="81efe-119">Member can read any messages.</span></span>
    
<span data-ttu-id="81efe-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="81efe-120">frightsCreate</span></span>
  
> <span data-ttu-id="81efe-121">El miembro puede crear mensajes.</span><span class="sxs-lookup"><span data-stu-id="81efe-121">Member can create messages.</span></span>
    
<span data-ttu-id="81efe-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="81efe-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="81efe-123">El miembro puede editar cualquier mensaje que pertenezca al usuario.</span><span class="sxs-lookup"><span data-stu-id="81efe-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="81efe-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="81efe-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="81efe-125">El miembro puede eliminar cualquier mensaje que pertenezca al usuario.</span><span class="sxs-lookup"><span data-stu-id="81efe-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="81efe-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="81efe-126">frightsEditAny</span></span>
  
> <span data-ttu-id="81efe-127">El miembro puede editar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="81efe-127">Member can edit any message.</span></span>
    
<span data-ttu-id="81efe-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="81efe-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="81efe-129">El miembro puede eliminar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="81efe-129">Member can delete any message.</span></span>
    
<span data-ttu-id="81efe-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="81efe-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="81efe-131">Member puede crear subcarpetas para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="81efe-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="81efe-132">frightsOwner</span></span>
  
> <span data-ttu-id="81efe-133">El miembro tiene todos los derechos anteriores en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="81efe-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="81efe-134">frightsContact</span></span>
  
> <span data-ttu-id="81efe-135">El miembro puede hacer que su nombre aparezca como el contacto en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="81efe-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="81efe-136">frightsVisible</span></span>
  
> <span data-ttu-id="81efe-137">El miembro puede ver que la carpeta existe.</span><span class="sxs-lookup"><span data-stu-id="81efe-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="81efe-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="81efe-138">rightsNone</span></span>
  
> <span data-ttu-id="81efe-139">El miembro no tiene derechos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="81efe-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="81efe-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="81efe-141">El miembro puede leer cualquier mensaje de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="81efe-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="81efe-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="81efe-143">El miembro puede leer y escribir en cualquier mensaje de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="81efe-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="81efe-144">rightsAll</span></span>
  
> <span data-ttu-id="81efe-145">El miembro tiene todos los derechos anteriores en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="81efe-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="81efe-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81efe-147">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="81efe-147">Protocol specifications</span></span>

<span data-ttu-id="81efe-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81efe-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81efe-149">Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="81efe-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81efe-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81efe-150">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81efe-151">Controla las operaciones de carpeta.</span><span class="sxs-lookup"><span data-stu-id="81efe-151">Handles folder operations.</span></span>
    
<span data-ttu-id="81efe-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81efe-152">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81efe-153">Controla la recuperación de listas de permisos de carpetas que se almacenan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="81efe-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="81efe-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81efe-154">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81efe-155">Especifica los métodos para conectarse a los buzones y configurarlos como delegados, e interacciones con los elementos de calendario y mensajes cuando actúan en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="81efe-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81efe-156">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="81efe-156">Header files</span></span>

<span data-ttu-id="81efe-157">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="81efe-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="81efe-158">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="81efe-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="81efe-159">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="81efe-159">Mapitags.h</span></span>
  
> <span data-ttu-id="81efe-160">Contiene definiciones de propiedades que se enumeran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="81efe-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81efe-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="81efe-161">See also</span></span>



[<span data-ttu-id="81efe-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81efe-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="81efe-163">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="81efe-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81efe-164">Propiedades canónicas de MAPI</span><span class="sxs-lookup"><span data-stu-id="81efe-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81efe-165">Asignar nombres de propiedad canónica a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="81efe-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81efe-166">Asignar nombres MAPI a nombres de propiedades canónicas</span><span class="sxs-lookup"><span data-stu-id="81efe-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

