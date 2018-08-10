---
title: Probar a seguir y dejar de seguir a personas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: En este tema se describe escenarios para comprobar la capacidad de un proveedor de Outlook Social Connector (OSC) que se deben seguir a un amigo y para detener el seguimiento de un amigo en la red social.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821209"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="a4f45-103">Probar a seguir y dejar de seguir a personas</span><span class="sxs-lookup"><span data-stu-id="a4f45-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="a4f45-104">En este tema se describe escenarios para comprobar la capacidad de un proveedor de Outlook Social Connector (OSC) que se deben seguir a un amigo y para detener el seguimiento de un amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="a4f45-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="a4f45-105">Seguimiento de una persona</span><span class="sxs-lookup"><span data-stu-id="a4f45-105">Following a person</span></span>

<span data-ttu-id="a4f45-106">Para seguir a una persona es agregar a una persona como amigo en la red social, utilizando la dirección SMTP proporcionada por el elemento seleccionado de Outlook.</span><span class="sxs-lookup"><span data-stu-id="a4f45-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="a4f45-107">Seguimiento de una persona en una red social normalmente implica que se solicita el permiso de esa persona por un correo electrónico a esa dirección SMTP.</span><span class="sxs-lookup"><span data-stu-id="a4f45-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="a4f45-108">Para poder conceder permiso, esa persona debe tener esa dirección SMTP ya incluida en su cuenta de redes sociales, o ser dispuesto a agregar que SMTP a una cuenta de redes sociales.</span><span class="sxs-lookup"><span data-stu-id="a4f45-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="a4f45-109">Pruebe cada uno de los siguientes escenarios para comprobar que su proveedor de OSC se comporta correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4f45-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="a4f45-110">**Escenario**</span><span class="sxs-lookup"><span data-stu-id="a4f45-110">**Scenario**</span></span>|<span data-ttu-id="a4f45-111">**Comportamiento esperado**</span><span class="sxs-lookup"><span data-stu-id="a4f45-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4f45-112">Si se intenta seguir a una persona en la red social que existe en la red social.</span><span class="sxs-lookup"><span data-stu-id="a4f45-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="a4f45-113">Para una red social que no requiere el permiso de la persona, la red social agrega inmediatamente a la persona como amigo.</span><span class="sxs-lookup"><span data-stu-id="a4f45-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="a4f45-114">Para una red que requiere el permiso de esa persona, la red social envía una notificación.</span><span class="sxs-lookup"><span data-stu-id="a4f45-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="a4f45-115">El panel de personas de Outlook muestra un icono pendiente de esa persona.</span><span class="sxs-lookup"><span data-stu-id="a4f45-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="a4f45-116">Si se intenta seguir a una persona en la red social que no existe en la red social.</span><span class="sxs-lookup"><span data-stu-id="a4f45-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="a4f45-117">El proveedor de OSC muestra el error correspondiente en [ISocialSession::FollowPerson](isocialsession-followperson.md) o [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span><span class="sxs-lookup"><span data-stu-id="a4f45-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="a4f45-118">Seguimiento de un amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="a4f45-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="a4f45-119">Para el amigo seleccionado en el panel de personas, se muestran tarjeta de identificación de la red social y la imagen del perfil de amigo para esa red social.</span><span class="sxs-lookup"><span data-stu-id="a4f45-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="a4f45-120">Al seleccionar el vínculo a la página de perfil de un amigo.</span><span class="sxs-lookup"><span data-stu-id="a4f45-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="a4f45-121">Página de amigo en la red social se abre en el explorador predeterminado del usuario que ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="a4f45-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="a4f45-122">Detener el seguimiento de una persona</span><span class="sxs-lookup"><span data-stu-id="a4f45-122">Stop following a person</span></span>

<span data-ttu-id="a4f45-123">Para detener el seguimiento de una persona es quitar a esa persona como amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="a4f45-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="a4f45-124">Probar el escenario siguiente para comprobar el deja de proveedor OSC siguiendo una persona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a4f45-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="a4f45-125">**Escenario**</span><span class="sxs-lookup"><span data-stu-id="a4f45-125">**Scenario**</span></span>|<span data-ttu-id="a4f45-126">**Comportamiento esperado**</span><span class="sxs-lookup"><span data-stu-id="a4f45-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4f45-127">Si se intenta quitar a una persona como amigo en la red social.</span><span class="sxs-lookup"><span data-stu-id="a4f45-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="a4f45-128">La red social ya no muestra a esa persona como amigo en la cuenta de usuario ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="a4f45-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4f45-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4f45-129">See also</span></span>

- [<span data-ttu-id="a4f45-130">Prepararse liberar un proveedor de OSC</span><span class="sxs-lookup"><span data-stu-id="a4f45-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

