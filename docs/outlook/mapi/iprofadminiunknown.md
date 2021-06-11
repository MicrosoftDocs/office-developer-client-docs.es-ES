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
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434119"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="0174b-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0174b-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="0174b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0174b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0174b-105">Admite la administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="0174b-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0174b-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0174b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0174b-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="0174b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="0174b-108">Expuesto por:</span><span class="sxs-lookup"><span data-stu-id="0174b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="0174b-109">Objeto de administración de perfiles</span><span class="sxs-lookup"><span data-stu-id="0174b-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="0174b-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="0174b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="0174b-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0174b-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="0174b-112">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="0174b-112">Called by:</span></span>  <br/> |<span data-ttu-id="0174b-113">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="0174b-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="0174b-114">Identificador de interfaz:</span><span class="sxs-lookup"><span data-stu-id="0174b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="0174b-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="0174b-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="0174b-116">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="0174b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="0174b-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="0174b-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="0174b-118">Orden de Vtable</span><span class="sxs-lookup"><span data-stu-id="0174b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="0174b-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="0174b-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="0174b-120">Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en un objeto de administración de perfiles.</span><span class="sxs-lookup"><span data-stu-id="0174b-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="0174b-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="0174b-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="0174b-122">Proporciona acceso a la tabla de perfiles, una tabla que contiene información sobre todos los perfiles disponibles.</span><span class="sxs-lookup"><span data-stu-id="0174b-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="0174b-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="0174b-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="0174b-124">Crea un nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="0174b-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="0174b-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="0174b-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="0174b-126">Elimina un perfil.</span><span class="sxs-lookup"><span data-stu-id="0174b-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="0174b-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="0174b-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="0174b-128">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0174b-128">Deprecated.</span></span> <span data-ttu-id="0174b-129">Cambia la contraseña de un perfil.</span><span class="sxs-lookup"><span data-stu-id="0174b-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="0174b-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="0174b-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="0174b-131">Copia un perfil.</span><span class="sxs-lookup"><span data-stu-id="0174b-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="0174b-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="0174b-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="0174b-133">Asigna un nuevo nombre a un perfil.</span><span class="sxs-lookup"><span data-stu-id="0174b-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="0174b-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0174b-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="0174b-135">Establece o borra el perfil predeterminado de un cliente.</span><span class="sxs-lookup"><span data-stu-id="0174b-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="0174b-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="0174b-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="0174b-137">Proporciona acceso a un objeto de administración del servicio de mensajes para realizar cambios en los servicios de mensajes en un perfil.</span><span class="sxs-lookup"><span data-stu-id="0174b-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0174b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0174b-138">See also</span></span>



[<span data-ttu-id="0174b-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="0174b-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

