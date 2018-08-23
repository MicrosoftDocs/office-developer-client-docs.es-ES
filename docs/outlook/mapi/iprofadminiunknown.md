---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 28dd45f29610b7ad56b4d3302715311569d497c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577418"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="135c3-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="135c3-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="135c3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="135c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="135c3-105">Admite la administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="135c3-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="135c3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="135c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="135c3-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="135c3-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="135c3-108">Expuestos por:</span><span class="sxs-lookup"><span data-stu-id="135c3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="135c3-109">Objeto de perfil de administración</span><span class="sxs-lookup"><span data-stu-id="135c3-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="135c3-110">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="135c3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="135c3-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="135c3-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="135c3-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="135c3-112">Called by:</span></span>  <br/> |<span data-ttu-id="135c3-113">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="135c3-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="135c3-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="135c3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="135c3-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="135c3-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="135c3-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="135c3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="135c3-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="135c3-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="135c3-118">Orden vtable</span><span class="sxs-lookup"><span data-stu-id="135c3-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="135c3-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="135c3-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="135c3-120">Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjeron en un objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="135c3-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="135c3-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="135c3-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="135c3-122">Proporciona acceso a la tabla de perfil, una tabla que contiene información acerca de todos los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="135c3-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="135c3-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="135c3-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="135c3-124">Crea un nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="135c3-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="135c3-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="135c3-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="135c3-126">Elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="135c3-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="135c3-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="135c3-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="135c3-128">En desuso.</span><span class="sxs-lookup"><span data-stu-id="135c3-128">Deprecated.</span></span> <span data-ttu-id="135c3-129">Cambia la contraseña de un perfil.</span><span class="sxs-lookup"><span data-stu-id="135c3-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="135c3-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="135c3-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="135c3-131">Copia un perfil.</span><span class="sxs-lookup"><span data-stu-id="135c3-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="135c3-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="135c3-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="135c3-133">Asigna un nombre nuevo a un perfil.</span><span class="sxs-lookup"><span data-stu-id="135c3-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="135c3-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135c3-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="135c3-135">Establece o borra el perfil predeterminado de un cliente.</span><span class="sxs-lookup"><span data-stu-id="135c3-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="135c3-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="135c3-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="135c3-137">Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensaje en un perfil.</span><span class="sxs-lookup"><span data-stu-id="135c3-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="135c3-138">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="135c3-138">See also</span></span>



[<span data-ttu-id="135c3-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="135c3-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

