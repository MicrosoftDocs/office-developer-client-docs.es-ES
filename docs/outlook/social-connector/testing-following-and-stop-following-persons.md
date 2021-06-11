---
title: Probar a seguir y dejar de seguir a personas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: En este tema se describen escenarios para probar la capacidad del proveedor de Outlook Social Connector (OSC) de seguir a un amigo y dejar de seguir a un amigo en la red social.
ms.openlocfilehash: 06a2bc48fa723f4d4513376cace96a195cef9fa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432453"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="f4e81-103">Probar a seguir y dejar de seguir a personas</span><span class="sxs-lookup"><span data-stu-id="f4e81-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="f4e81-104">En este tema se describen escenarios para probar la capacidad del proveedor de Outlook Social Connector (OSC) de seguir a un amigo y dejar de seguir a un amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="f4e81-105">Seguir a una persona</span><span class="sxs-lookup"><span data-stu-id="f4e81-105">Following a person</span></span>

<span data-ttu-id="f4e81-106">Seguir a una persona es agregar una persona como un amigo en la red social, usando la dirección SMTP proporcionada por el elemento Outlook seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f4e81-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="f4e81-107">Seguir a alguien en una red social suele implicar solicitar permiso a esa persona mediante un correo electrónico a esa dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="f4e81-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="f4e81-108">Para conceder permiso, esa persona debe tener esa dirección SMTP ya incluida en su cuenta de red social o estar dispuesta a agregar ese SMTP a una cuenta de red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="f4e81-109">Pruebe cada uno de los siguientes escenarios para comprobar que el proveedor de OSC se comporta correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4e81-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="f4e81-110">**Escenario**</span><span class="sxs-lookup"><span data-stu-id="f4e81-110">**Scenario**</span></span>|<span data-ttu-id="f4e81-111">**Comportamiento esperado**</span><span class="sxs-lookup"><span data-stu-id="f4e81-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4e81-112">Intentar seguir a una persona de la red social que existe en la red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="f4e81-113">Para una red social que no requiere permiso de la persona, la red social agrega inmediatamente a la persona como un amigo.</span><span class="sxs-lookup"><span data-stu-id="f4e81-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="f4e81-114">Para una red que requiere permiso de esa persona, la red social envía una notificación.</span><span class="sxs-lookup"><span data-stu-id="f4e81-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="f4e81-115">El Outlook de personas muestra un icono pendiente para esa persona.</span><span class="sxs-lookup"><span data-stu-id="f4e81-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="f4e81-116">Intentar seguir a una persona en la red social que no existe en la red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="f4e81-117">El proveedor de OSC muestra el error adecuado en [ISocialSession::FollowPerson](isocialsession-followperson.md) o [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span><span class="sxs-lookup"><span data-stu-id="f4e81-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="f4e81-118">Seguir a un amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="f4e81-119">Para el amigo seleccionado en el Panel de personas, se muestran el distintivo de la red social y la imagen de perfil del amigo para esa red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="f4e81-120">Seleccionar el vínculo a la página de perfil de un amigo.</span><span class="sxs-lookup"><span data-stu-id="f4e81-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="f4e81-121">La página del amigo en la red social se abre en el explorador predeterminado del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="f4e81-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="f4e81-122">Dejar de seguir a una persona</span><span class="sxs-lookup"><span data-stu-id="f4e81-122">Stop following a person</span></span>

<span data-ttu-id="f4e81-123">Para dejar de seguir a una persona es quitar a esa persona como un amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="f4e81-124">Pruebe el siguiente escenario para comprobar que el proveedor de OSC deja de seguir a una persona correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4e81-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="f4e81-125">**Escenario**</span><span class="sxs-lookup"><span data-stu-id="f4e81-125">**Scenario**</span></span>|<span data-ttu-id="f4e81-126">**Comportamiento esperado**</span><span class="sxs-lookup"><span data-stu-id="f4e81-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f4e81-127">Intentar quitar a una persona como un amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="f4e81-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="f4e81-128">La red social ya no enumera a esa persona como un amigo en la cuenta del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="f4e81-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f4e81-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4e81-129">See also</span></span>

- [<span data-ttu-id="f4e81-130">Prepararse para liberar un proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="f4e81-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

