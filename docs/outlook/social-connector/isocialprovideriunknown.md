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
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409961"
---
# <a name="isocialprovider--iunknown"></a><span data-ttu-id="26b49-103">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26b49-103">ISocialProvider : IUnknown</span></span>

<span data-ttu-id="26b49-104">Representa una instancia de un proveedor de Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="26b49-104">Represents an instance of an Outlook Social Connector (OSC) provider.</span></span>
  
## <a name="members"></a><span data-ttu-id="26b49-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="26b49-105">Members</span></span>

<span data-ttu-id="26b49-106">En la tabla siguiente se muestran los miembros que están disponibles en la **interfaz ISocialProvider.**</span><span class="sxs-lookup"><span data-stu-id="26b49-106">The following table shows the members that are available on the **ISocialProvider** interface.</span></span> 
  
|<span data-ttu-id="26b49-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="26b49-107">**Name**</span></span>|<span data-ttu-id="26b49-108">**Tipo de miembro**</span><span class="sxs-lookup"><span data-stu-id="26b49-108">**Member type**</span></span>|<span data-ttu-id="26b49-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26b49-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="26b49-110">DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="26b49-110">DefaultSiteUrls</span></span>](isocialprovider-defaultsiteurls.md) <br/> |<span data-ttu-id="26b49-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26b49-111">Property</span></span>  <br/> |<span data-ttu-id="26b49-112">Devuelve una matriz de cadenas que especifican direcciones URL de sitio para el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="26b49-112">Returns an array of strings that specify site URLs for the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="26b49-113">GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="26b49-113">GetAutoConfiguredSession</span></span>](isocialprovider-getautoconfiguredsession.md) <br/> |<span data-ttu-id="26b49-114">Method</span><span class="sxs-lookup"><span data-stu-id="26b49-114">Method</span></span>  <br/> |<span data-ttu-id="26b49-115">Obtiene una interfaz [ISocialSession](isocialsessioniunknown.md) configurada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="26b49-115">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="26b49-116">GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="26b49-116">GetCapabilities</span></span>](isocialprovider-getcapabilities.md) <br/> |<span data-ttu-id="26b49-117">Method</span><span class="sxs-lookup"><span data-stu-id="26b49-117">Method</span></span>  <br/> |<span data-ttu-id="26b49-118">Obtiene una cadena que describe las capacidades del proveedor.</span><span class="sxs-lookup"><span data-stu-id="26b49-118">Gets a string that describes provider capabilities.</span></span>  <br/> |
|[<span data-ttu-id="26b49-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="26b49-119">GetSession</span></span>](isocialprovider-getsession.md) <br/> |<span data-ttu-id="26b49-120">Method</span><span class="sxs-lookup"><span data-stu-id="26b49-120">Method</span></span>  <br/> |<span data-ttu-id="26b49-121">Obtiene una [interfaz ISocialSession.](isocialsessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="26b49-121">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span>  <br/> |
|[<span data-ttu-id="26b49-122">GetStatusSettings</span><span class="sxs-lookup"><span data-stu-id="26b49-122">GetStatusSettings</span></span>](isocialprovider-getstatussettings.md) <br/> |<span data-ttu-id="26b49-123">Method</span><span class="sxs-lookup"><span data-stu-id="26b49-123">Method</span></span>  <br/> |<span data-ttu-id="26b49-124">Este método no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="26b49-124">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="26b49-125">Load</span><span class="sxs-lookup"><span data-stu-id="26b49-125">Load</span></span>](isocialprovider-load.md) <br/> |<span data-ttu-id="26b49-126">Method</span><span class="sxs-lookup"><span data-stu-id="26b49-126">Method</span></span>  <br/> |<span data-ttu-id="26b49-127">Inicializa el proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="26b49-127">Initializes the OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="26b49-128">SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="26b49-128">SocialNetworkGuid</span></span>](isocialprovider-socialnetworkguid.md) <br/> |<span data-ttu-id="26b49-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26b49-129">Property</span></span>  <br/> |<span data-ttu-id="26b49-130">Devuelve un GUID que representa un identificador único para la red social.</span><span class="sxs-lookup"><span data-stu-id="26b49-130">Returns a GUID that represents a unique identifier for the social network.</span></span>  <br/> |
|[<span data-ttu-id="26b49-131">SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="26b49-131">SocialNetworkIcon</span></span>](isocialprovider-socialnetworkicon.md) <br/> |<span data-ttu-id="26b49-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26b49-132">Property</span></span>  <br/> |<span data-ttu-id="26b49-133">Devuelve una matriz de bytes que representa el icono de la red social.</span><span class="sxs-lookup"><span data-stu-id="26b49-133">Returns an array of bytes that represents the icon for the social network.</span></span>  <br/> |
|[<span data-ttu-id="26b49-134">SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="26b49-134">SocialNetworkName</span></span>](isocialprovider-socialnetworkname.md) <br/> |<span data-ttu-id="26b49-135">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26b49-135">Property</span></span>  <br/> |<span data-ttu-id="26b49-136">Devuelve una cadena que representa el nombre de la red social.</span><span class="sxs-lookup"><span data-stu-id="26b49-136">Returns a string that represents the social network name.</span></span>  <br/> |
|[<span data-ttu-id="26b49-137">Versión</span><span class="sxs-lookup"><span data-stu-id="26b49-137">Version</span></span>](isocialprovider-version.md) <br/> |<span data-ttu-id="26b49-138">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26b49-138">Property</span></span>  <br/> |<span data-ttu-id="26b49-139">Devuelve una cadena que representa el número de versión del proveedor de esta red social.</span><span class="sxs-lookup"><span data-stu-id="26b49-139">Returns a string that represents the version number of the provider for this social network.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26b49-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26b49-140">Remarks</span></span>

<span data-ttu-id="26b49-141">Un proveedor de OSC debe implementar esta interfaz para comunicarse con el OSC.</span><span class="sxs-lookup"><span data-stu-id="26b49-141">An OSC provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26b49-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="26b49-142">See also</span></span>

- [<span data-ttu-id="26b49-143">Interfaces de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="26b49-143">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

