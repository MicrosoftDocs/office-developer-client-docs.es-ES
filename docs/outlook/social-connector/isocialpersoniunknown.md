---
title: ISocialPerson IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a2fa12-a7ef-4a95-9875-72ec6f8ceac9
description: Representa a una persona de la red social.
ms.openlocfilehash: 0ad129b0fc15fc9f3ccdf1cff7d8519bb07b024e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407014"
---
# <a name="isocialperson--iunknown"></a><span data-ttu-id="77855-103">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77855-103">ISocialPerson : IUnknown</span></span>

<span data-ttu-id="77855-104">Representa a una persona de la red social.</span><span class="sxs-lookup"><span data-stu-id="77855-104">Represents a person on the social network.</span></span>
  
## <a name="members"></a><span data-ttu-id="77855-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="77855-105">Members</span></span>

<span data-ttu-id="77855-106">En la tabla siguiente se muestran los miembros que están disponibles en la **interfaz ISocialPerson.**</span><span class="sxs-lookup"><span data-stu-id="77855-106">The following table shows the members that are available on the **ISocialPerson** interface.</span></span> 
  
|<span data-ttu-id="77855-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="77855-107">**Name**</span></span>|<span data-ttu-id="77855-108">**Tipo de miembro**</span><span class="sxs-lookup"><span data-stu-id="77855-108">**Member type**</span></span>|<span data-ttu-id="77855-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="77855-109">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="77855-110">GetActivities</span><span class="sxs-lookup"><span data-stu-id="77855-110">GetActivities</span></span>](isocialperson-getactivities.md) <br/> |<span data-ttu-id="77855-111">Method</span><span class="sxs-lookup"><span data-stu-id="77855-111">Method</span></span>  <br/> |<span data-ttu-id="77855-112">Este método está en desuso desde Outlook Social Connector 2013.</span><span class="sxs-lookup"><span data-stu-id="77855-112">This method has been deprecated since Outlook Social Connector 2013.</span></span>  <br/> |
|[<span data-ttu-id="77855-113">GetDetails</span><span class="sxs-lookup"><span data-stu-id="77855-113">GetDetails</span></span>](isocialperson-getdetails.md) <br/> |<span data-ttu-id="77855-114">Method</span><span class="sxs-lookup"><span data-stu-id="77855-114">Method</span></span>  <br/> |<span data-ttu-id="77855-115">Obtiene una cadena que representa los detalles de la persona, como el nombre, los apellidos y una dirección URL de una imagen de perfil.</span><span class="sxs-lookup"><span data-stu-id="77855-115">Gets a string that represents details for the person, such as the first name, last name, and a URL to a profile picture.</span></span>  <br/> |
|[<span data-ttu-id="77855-116">GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="77855-116">GetFriendsAndColleagues</span></span>](isocialperson-getfriendsandcolleagues.md) <br/> |<span data-ttu-id="77855-117">Method</span><span class="sxs-lookup"><span data-stu-id="77855-117">Method</span></span>  <br/> |<span data-ttu-id="77855-118">Obtiene una cadena que representa una colección de personas.</span><span class="sxs-lookup"><span data-stu-id="77855-118">Gets a string that represents a collection of people.</span></span>  <br/> |
|[<span data-ttu-id="77855-119">GetFriendsAndColleaguesIDs</span><span class="sxs-lookup"><span data-stu-id="77855-119">GetFriendsAndColleaguesIDs</span></span>](isocialperson-getfriendsandcolleaguesids.md) <br/> |<span data-ttu-id="77855-120">Method</span><span class="sxs-lookup"><span data-stu-id="77855-120">Method</span></span>  <br/> |<span data-ttu-id="77855-121">Este método no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="77855-121">This method is currently not supported.</span></span>  <br/> |
|[<span data-ttu-id="77855-122">GetPicture</span><span class="sxs-lookup"><span data-stu-id="77855-122">GetPicture</span></span>](isocialperson-getpicture.md) <br/> |<span data-ttu-id="77855-123">Method</span><span class="sxs-lookup"><span data-stu-id="77855-123">Method</span></span>  <br/> |<span data-ttu-id="77855-124">Obtiene una matriz de bytes que contiene el recurso de imagen de la persona.</span><span class="sxs-lookup"><span data-stu-id="77855-124">Gets an array of bytes that contains the picture resource for the person.</span></span>  <br/> |
|[<span data-ttu-id="77855-125">GetStatus</span><span class="sxs-lookup"><span data-stu-id="77855-125">GetStatus</span></span>](isocialperson-getstatus.md) <br/> |<span data-ttu-id="77855-126">Method</span><span class="sxs-lookup"><span data-stu-id="77855-126">Method</span></span>  <br/> |<span data-ttu-id="77855-127">Este método no se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="77855-127">This method is currently not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77855-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="77855-128">Remarks</span></span>

<span data-ttu-id="77855-129">Un proveedor de Outlook Social Connector (OSC) debe implementar esta interfaz para comunicarse con el OSC.</span><span class="sxs-lookup"><span data-stu-id="77855-129">An Outlook Social Connector (OSC) provider must implement this interface to communicate with the OSC.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77855-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="77855-130">See also</span></span>

- [<span data-ttu-id="77855-131">Interfaces de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="77855-131">Outlook Social Connector Provider Interfaces</span></span>](outlook-social-connector-provider-interfaces.md)

