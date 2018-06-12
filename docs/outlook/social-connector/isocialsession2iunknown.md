---
title: ISocialSession2 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f516e86e-0158-472b-9711-fe7491b24404
description: Admite la adición de amigos, sincronización a petición o híbrido de amigos, sincronización a petición de actividades, o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché.
ms.openlocfilehash: b14804d35e54ebe9fe2a529fb2664f0a661653bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821130"
---
# <a name="isocialsession2--iunknown"></a><span data-ttu-id="a1d3f-103">ISocialSession2: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1d3f-103">ISocialSession2 : IUnknown</span></span>

<span data-ttu-id="a1d3f-104">Admite la adición de amigos, sincronización a petición o híbrido de amigos, sincronización a petición de actividades, o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="a1d3f-104">Supports adding friends, on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span>
  
## <a name="members"></a><span data-ttu-id="a1d3f-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1d3f-105">Members</span></span>

<span data-ttu-id="a1d3f-106">La siguiente tabla muestran a los miembros que están disponibles en la interfaz **ISocialSession2** .</span><span class="sxs-lookup"><span data-stu-id="a1d3f-106">The following table shows the members that are available on the **ISocialSession2** interface.</span></span> 
  
|<span data-ttu-id="a1d3f-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="a1d3f-107">**Name**</span></span>|<span data-ttu-id="a1d3f-108">**Tipo de miembro**</span><span class="sxs-lookup"><span data-stu-id="a1d3f-108">**Member type**</span></span>|<span data-ttu-id="a1d3f-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a1d3f-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1d3f-110">FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="a1d3f-110">FollowPersonEx</span></span>](isocialsession2-followpersonex.md) <br/> |<span data-ttu-id="a1d3f-111">Método</span><span class="sxs-lookup"><span data-stu-id="a1d3f-111">Method</span></span>  <br/> |<span data-ttu-id="a1d3f-112">Agrega a la persona identificada por los parámetros _emailAddresses_ y _displayName_ como amigo para el usuario ha iniciado sesión en la red social.</span><span class="sxs-lookup"><span data-stu-id="a1d3f-112">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span>  <br/> |
|[<span data-ttu-id="a1d3f-113">GetActivitiesEx</span><span class="sxs-lookup"><span data-stu-id="a1d3f-113">GetActivitiesEx</span></span>](isocialsession2-getactivitiesex.md) <br/> |<span data-ttu-id="a1d3f-114">Método</span><span class="sxs-lookup"><span data-stu-id="a1d3f-114">Method</span></span>  <br/> |<span data-ttu-id="a1d3f-115">Obtiene una cadena que representa una colección de las actividades de los usuarios especificados por el parámetro _hashedAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="a1d3f-115">Gets a string that represents a collection of activities of the users specified by the  _hashedAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="a1d3f-116">GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="a1d3f-116">GetPeopleDetails</span></span>](isocialsession2-getpeopledetails.md) <br/> |<span data-ttu-id="a1d3f-117">Método</span><span class="sxs-lookup"><span data-stu-id="a1d3f-117">Method</span></span>  <br/> |<span data-ttu-id="a1d3f-118">Devuelve una cadena que contiene una colección de detalles de imagen y la persona para los usuarios especificados por el parámetro _personsAddresses_ .</span><span class="sxs-lookup"><span data-stu-id="a1d3f-118">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span>  <br/> |
|[<span data-ttu-id="a1d3f-119">LogonCached</span><span class="sxs-lookup"><span data-stu-id="a1d3f-119">LogonCached</span></span>](isocialsession2-logoncached.md) <br/> |<span data-ttu-id="a1d3f-120">Método</span><span class="sxs-lookup"><span data-stu-id="a1d3f-120">Method</span></span>  <br/> |<span data-ttu-id="a1d3f-121">Inicie sesión en el sitio de red social mediante credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="a1d3f-121">Logs on to the social network site using cached credentials.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1d3f-122">Notas</span><span class="sxs-lookup"><span data-stu-id="a1d3f-122">Remarks</span></span>

<span data-ttu-id="a1d3f-123">Puede elegir un proveedor de Outlook Social Connector (OSC) implementar esta interfaz si el proveedor admite la sincronización a petición o híbrido de amigos, sincronización a petición de actividades, o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="a1d3f-123">An Outlook Social Connector (OSC) provider can choose to implement this interface if the provider supports on-demand or hybrid synchronization of friends, on-demand synchronization of activities, or logging on to the social network by using cached credentials.</span></span> <span data-ttu-id="a1d3f-124">Si el proveedor de OSC implementa **ISocialSession2** y admite las siguientes a personas en la red social, el OSC llamaría a [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) en lugar de [ISocialSession::FollowPerson](isocialsession-followperson.md), y el proveedor debe implementar **ISocialSession2::FollowPersonEx**, así como.</span><span class="sxs-lookup"><span data-stu-id="a1d3f-124">If the OSC provider implements **ISocialSession2** and supports following persons on the social network, the OSC would call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of [ISocialSession::FollowPerson](isocialsession-followperson.md), and the provider must implement **ISocialSession2::FollowPersonEx**, as well.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a1d3f-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="a1d3f-125">See also</span></span>

- [<span data-ttu-id="a1d3f-126">Interfaces del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="a1d3f-126">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

