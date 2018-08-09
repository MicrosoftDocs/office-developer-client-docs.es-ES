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
ms.openlocfilehash: 2ffc6973d2670402ec8095120eea3db02f529d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819732"
---
# <a name="pidtagmemberrights-canonical-property"></a><span data-ttu-id="d7bb6-103">Propiedad canónica PidTagMemberRights</span><span class="sxs-lookup"><span data-stu-id="d7bb6-103">PidTagMemberRights Canonical Property</span></span>

  
  
<span data-ttu-id="d7bb6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7bb6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7bb6-105">Contiene un conjunto de bits que indica los derechos de este miembro en una carpeta o un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-105">Contains a set of bits that indicated the rights of this member on a folder or mailbox.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7bb6-106">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="d7bb6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7bb6-107">PR_MEMBER_RIGHTS</span><span class="sxs-lookup"><span data-stu-id="d7bb6-107">PR_MEMBER_RIGHTS</span></span>  <br/> |
|<span data-ttu-id="d7bb6-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d7bb6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7bb6-109">0x6673</span><span class="sxs-lookup"><span data-stu-id="d7bb6-109">0x6673</span></span>  <br/> |
|<span data-ttu-id="d7bb6-110">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="d7bb6-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7bb6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d7bb6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d7bb6-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d7bb6-112">Area:</span></span>  <br/> |<span data-ttu-id="d7bb6-113">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="d7bb6-113">Access Control</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7bb6-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d7bb6-114">Remarks</span></span>

<span data-ttu-id="d7bb6-115">Esta propiedad se utiliza con la interfaz [IExchangeModifyTable](iexchangemodifytableiunknown.md) para definir los derechos de un miembro en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-115">This property is used by the [IExchangeModifyTable](iexchangemodifytableiunknown.md) interface to define rights of a member on a folder.</span></span> <span data-ttu-id="d7bb6-116">Estos derechos se pueden mostrar y modificar.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-116">These rights can be displayed and modified.</span></span> <span data-ttu-id="d7bb6-117">Los siguientes valores son los derechos definidos para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-117">The following values are rights defined for this property.</span></span> 
  
<span data-ttu-id="d7bb6-118">frightsReadAny</span><span class="sxs-lookup"><span data-stu-id="d7bb6-118">frightsReadAny</span></span>
  
> <span data-ttu-id="d7bb6-119">Miembros pueden leer todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-119">Member can read any messages.</span></span>
    
<span data-ttu-id="d7bb6-120">frightsCreate</span><span class="sxs-lookup"><span data-stu-id="d7bb6-120">frightsCreate</span></span>
  
> <span data-ttu-id="d7bb6-121">Miembros pueden crear mensajes.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-121">Member can create messages.</span></span>
    
<span data-ttu-id="d7bb6-122">frightsEditOwned</span><span class="sxs-lookup"><span data-stu-id="d7bb6-122">frightsEditOwned</span></span>
  
> <span data-ttu-id="d7bb6-123">Miembros pueden editar todos los mensajes que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-123">Member can edit any messages owned by the user.</span></span>
    
<span data-ttu-id="d7bb6-124">frightsDeleteOwned</span><span class="sxs-lookup"><span data-stu-id="d7bb6-124">frightsDeleteOwned</span></span>
  
> <span data-ttu-id="d7bb6-125">Miembro puede eliminar todos los mensajes que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-125">Member can delete any messages owned by the user.</span></span>
    
<span data-ttu-id="d7bb6-126">frightsEditAny</span><span class="sxs-lookup"><span data-stu-id="d7bb6-126">frightsEditAny</span></span>
  
> <span data-ttu-id="d7bb6-127">Miembro puede editar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-127">Member can edit any message.</span></span>
    
<span data-ttu-id="d7bb6-128">frightsDeleteAny</span><span class="sxs-lookup"><span data-stu-id="d7bb6-128">frightsDeleteAny</span></span>
  
> <span data-ttu-id="d7bb6-129">Miembro puede eliminar cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-129">Member can delete any message.</span></span>
    
<span data-ttu-id="d7bb6-130">frightsCreateSubfolder</span><span class="sxs-lookup"><span data-stu-id="d7bb6-130">frightsCreateSubfolder</span></span>
  
> <span data-ttu-id="d7bb6-131">Miembro puede crear subcarpetas para la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-131">Member can create subfolders for the folder.</span></span>
    
<span data-ttu-id="d7bb6-132">frightsOwner</span><span class="sxs-lookup"><span data-stu-id="d7bb6-132">frightsOwner</span></span>
  
> <span data-ttu-id="d7bb6-133">Miembro tiene todos los derechos anteriores en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-133">Member has all the previous rights on the folder.</span></span>
    
<span data-ttu-id="d7bb6-134">frightsContact</span><span class="sxs-lookup"><span data-stu-id="d7bb6-134">frightsContact</span></span>
  
> <span data-ttu-id="d7bb6-135">Miembro puede tener su nombre aparecen como el contacto en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-135">Member can have your name appear as the contact on the folder.</span></span>
    
<span data-ttu-id="d7bb6-136">frightsVisible</span><span class="sxs-lookup"><span data-stu-id="d7bb6-136">frightsVisible</span></span>
  
> <span data-ttu-id="d7bb6-137">Miembro puede ver que existe la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-137">Member can see that the folder exists.</span></span>
    
<span data-ttu-id="d7bb6-138">rightsNone</span><span class="sxs-lookup"><span data-stu-id="d7bb6-138">rightsNone</span></span>
  
> <span data-ttu-id="d7bb6-139">Miembro no tiene derechos en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-139">Member does not have rights on the folder.</span></span>
    
<span data-ttu-id="d7bb6-140">rightsReadOnly</span><span class="sxs-lookup"><span data-stu-id="d7bb6-140">rightsReadOnly</span></span>
  
> <span data-ttu-id="d7bb6-141">Miembros pueden leer los mensajes en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-141">Member can read any message in the folder.</span></span>
    
<span data-ttu-id="d7bb6-142">rightsReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7bb6-142">rightsReadWrite</span></span>
  
> <span data-ttu-id="d7bb6-143">Miembro puede leer desde y escribir en cualquier mensaje en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-143">Member can read from and write to any message in the folder.</span></span>
    
<span data-ttu-id="d7bb6-144">rightsAll</span><span class="sxs-lookup"><span data-stu-id="d7bb6-144">rightsAll</span></span>
  
> <span data-ttu-id="d7bb6-145">Miembro tiene todos los derechos anteriores en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-145">Member has all the previous rights on the folder.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d7bb6-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7bb6-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d7bb6-147">Especificaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="d7bb6-147">Protocol specifications</span></span>

<span data-ttu-id="d7bb6-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bb6-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bb6-149">Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d7bb6-150">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bb6-150">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bb6-151">Controla las operaciones de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-151">Handles folder operations.</span></span>
    
<span data-ttu-id="d7bb6-152">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bb6-152">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bb6-153">Controla la recuperación de listas de permisos de carpeta que se almacenan en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-153">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="d7bb6-154">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7bb6-154">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d7bb6-155">Especifica los métodos para conectarse a y configurar los buzones de correo como delegados y las interacciones con los elementos de mensaje y calendario cuando actúen en nombre de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-155">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar items when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d7bb6-156">Archivos de encabezado</span><span class="sxs-lookup"><span data-stu-id="d7bb6-156">Header files</span></span>

<span data-ttu-id="d7bb6-157">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7bb6-157">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7bb6-158">Proporciona definiciones de tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-158">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7bb6-159">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7bb6-159">Mapitags.h</span></span>
  
> <span data-ttu-id="d7bb6-160">Contiene las definiciones de propiedades que se muestran como propiedades asociadas.</span><span class="sxs-lookup"><span data-stu-id="d7bb6-160">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7bb6-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7bb6-161">See also</span></span>



[<span data-ttu-id="d7bb6-162">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d7bb6-162">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="d7bb6-163">Propiedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7bb6-163">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7bb6-164">Propiedades MAPI canónicas</span><span class="sxs-lookup"><span data-stu-id="d7bb6-164">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7bb6-165">Asignar nombres de propiedad canónicos a nombres MAPI</span><span class="sxs-lookup"><span data-stu-id="d7bb6-165">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7bb6-166">Asignar nombres MAPI a los nombres de propiedad canónico</span><span class="sxs-lookup"><span data-stu-id="d7bb6-166">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

