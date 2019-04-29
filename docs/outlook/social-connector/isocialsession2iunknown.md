---
title: IUnknown ISocialSession2
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Admite la adición de amigos, a petición o la sincronización híbrida de amigos, la sincronización a petición de actividades o el inicio de sesión en la red social mediante el uso de credenciales almacenadas en caché.
ms.openlocfilehash: 6dc581bb812408d7e01f94c375671783445616a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408834"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="0a776-103">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0a776-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="0a776-104">Admite la adición de amigos, a petición o la sincronización híbrida de amigos, la sincronización a petición de actividades o el inicio de sesión en la red social mediante el uso de credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="0a776-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="0a776-105">Members</span><span class="sxs-lookup"><span data-stu-id="0a776-105">Members</span></span>

<span data-ttu-id="0a776-106">En la siguiente tabla se muestran los miembros que están disponibles en la interfaz **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="0a776-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="0a776-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0a776-107">**Name**</span></span>|<span data-ttu-id="0a776-108">**Tipo de miembro**</span><span class="sxs-lookup"><span data-stu-id="0a776-108">**Member type**</span></span>|<span data-ttu-id="0a776-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a776-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0a776-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="0a776-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="0a776-111">Método</span><span class="sxs-lookup"><span data-stu-id="0a776-111">Method</span></span>  <br/> |<span data-ttu-id="0a776-112">Agrega la persona identificada por los parámetros _emailAddresses_ y _displayName_ como un amigo para el usuario que ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="0a776-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="0a776-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="0a776-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="0a776-114">Método</span><span class="sxs-lookup"><span data-stu-id="0a776-114">Method</span></span>  <br/> |<span data-ttu-id="0a776-115">Obtiene una cadena que representa una colección de actividades de los usuarios especificados por el parámetro _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="0a776-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="0a776-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="0a776-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="0a776-117">Método</span><span class="sxs-lookup"><span data-stu-id="0a776-117">Method</span></span>  <br/> |<span data-ttu-id="0a776-118">Devuelve una cadena que contiene una colección de personas y detalles de la imagen para los usuarios especificados por el parámetro _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="0a776-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="0a776-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="0a776-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="0a776-120">Método</span><span class="sxs-lookup"><span data-stu-id="0a776-120">Method</span></span>  <br/> |<span data-ttu-id="0a776-121">Inicia sesión en el sitio de red social con las credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="0a776-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a776-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a776-122">Remarks</span></span>

<span data-ttu-id="0a776-123">Un proveedor de Outlook Social Connector (OSC) puede optar por implementar esta interfaz si el proveedor admite la sincronización a petición o híbrida de amigos, la sincronización a petición de actividades o el inicio de sesión en la red social con las credenciales almacenadas en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0a776-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="0a776-124">Si el proveedor de OSC implementa **ISocialSession2** y admite seguimiento de personas en la red social, OSC llamaría a [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) en lugar de [ISocialSession:: FollowPerson](isocialsession-followperson.md)y el proveedor debe implementar **ISocialSession2:: FollowPersonEx**también.</span><span class="sxs-lookup"><span data-stu-id="0a776-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0a776-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="0a776-125">See also</span></span>

- [<span data-ttu-id="0a776-126">Interfaces de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="0a776-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

