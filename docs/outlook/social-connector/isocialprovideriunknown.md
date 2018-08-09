---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Representa una instancia de un proveedor de Outlook Social Connector (OSC).
ms.openlocfilehash: 912b2d92137febe80e0d97362e0a490f138b2e66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821233"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="82915-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="82915-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="82915-104">Representa una instancia de un proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="82915-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="82915-105">Members</span><span class="sxs-lookup"><span data-stu-id="82915-105">Members</span></span>

<span data-ttu-id="82915-106">La siguiente tabla muestran a los miembros que están disponibles en la interfaz **ISocialProvider** .</span><span class="sxs-lookup"><span data-stu-id="82915-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="82915-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="82915-107">**Name**</span></span>|<span data-ttu-id="82915-108">**Tipo de miembro**</span><span class="sxs-lookup"><span data-stu-id="82915-108">**Member type**</span></span>|<span data-ttu-id="82915-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="82915-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="82915-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="82915-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="82915-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82915-111">Property</span></span>  <br/> |<span data-ttu-id="82915-112">Devuelve una matriz de cadenas que especifican las direcciones URL de sitio para el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="82915-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="82915-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="82915-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="82915-114">Método</span><span class="sxs-lookup"><span data-stu-id="82915-114">Method</span></span>  <br/> |<span data-ttu-id="82915-115">Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="82915-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="82915-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="82915-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="82915-117">Método</span><span class="sxs-lookup"><span data-stu-id="82915-117">Method</span></span>  <br/> |<span data-ttu-id="82915-118">Obtiene una cadena que describe las capacidades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="82915-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="82915-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="82915-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="82915-120">Método</span><span class="sxs-lookup"><span data-stu-id="82915-120">Method</span></span>  <br/> |<span data-ttu-id="82915-121">Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="82915-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="82915-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="82915-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="82915-123">Método</span><span class="sxs-lookup"><span data-stu-id="82915-123">Method</span></span>  <br/> |<span data-ttu-id="82915-124">Este método no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="82915-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="82915-125">Load</span><span class="sxs-lookup"><span data-stu-id="82915-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="82915-126">Método</span><span class="sxs-lookup"><span data-stu-id="82915-126">Method</span></span>  <br/> |<span data-ttu-id="82915-127">Inicializa el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="82915-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="82915-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="82915-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="82915-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82915-129">Property</span></span>  <br/> |<span data-ttu-id="82915-130">Devuelve un GUID que representa un identificador único para la red social.</span><span class="sxs-lookup"><span data-stu-id="82915-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="82915-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="82915-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="82915-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82915-132">Property</span></span>  <br/> |<span data-ttu-id="82915-133">Devuelve una matriz de bytes que representa el icono para la red social.</span><span class="sxs-lookup"><span data-stu-id="82915-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="82915-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="82915-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="82915-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82915-135">Property</span></span>  <br/> |<span data-ttu-id="82915-136">Devuelve un valor de tipo string que representa el nombre de redes sociales.</span><span class="sxs-lookup"><span data-stu-id="82915-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="82915-137">Versión</span><span class="sxs-lookup"><span data-stu-id="82915-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="82915-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82915-138">Property</span></span>  <br/> |<span data-ttu-id="82915-139">Devuelve un valor de tipo string que representa el número de versión del proveedor para esta red social.</span><span class="sxs-lookup"><span data-stu-id="82915-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82915-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82915-140">Remarks</span></span>

<span data-ttu-id="82915-141">Un proveedor de OSC debe implementar esta interfaz para comunicarse con el OSC.</span><span class="sxs-lookup"><span data-stu-id="82915-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="82915-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="82915-142">See also</span></span>

- [<span data-ttu-id="82915-143">Interfaces del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="82915-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

