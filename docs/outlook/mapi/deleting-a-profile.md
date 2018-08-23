---
title: Eliminar un perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573246"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="8b137-103">Eliminar un perfil</span><span class="sxs-lookup"><span data-stu-id="8b137-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="8b137-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b137-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8b137-105">**Para eliminar un perfil**</span><span class="sxs-lookup"><span data-stu-id="8b137-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="8b137-106">Llame a [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="8b137-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="8b137-107">**DeleteProfile** marca el perfil para su eliminación, si se está usando, esperar hasta que ya no está activa para quitarla.</span><span class="sxs-lookup"><span data-stu-id="8b137-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="8b137-108">El perfil no desaparece realmente hasta que se ha desconectado todos los clientes con una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="8b137-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="8b137-109">**DeleteProfile** llama a la función de punto de entrada de cada servicio de mensajes en el perfil con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="8b137-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="8b137-110">Las llamadas a las funciones de punto de entrada se producen antes de que los servicios se encuentran físicamente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="8b137-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

