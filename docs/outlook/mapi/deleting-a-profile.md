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
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410206"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="2d47f-103">Eliminar un perfil</span><span class="sxs-lookup"><span data-stu-id="2d47f-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="2d47f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d47f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2d47f-105">**Para eliminar un perfil**</span><span class="sxs-lookup"><span data-stu-id="2d47f-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="2d47f-106">Llame [a IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="2d47f-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="2d47f-107">**DeleteProfile** marca el perfil para su eliminación si se está utilizando actualmente, esperando hasta que ya no esté activo para quitarlo.</span><span class="sxs-lookup"><span data-stu-id="2d47f-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="2d47f-108">El perfil no desaparece realmente hasta que todos los clientes con una sesión activa se desconectan.</span><span class="sxs-lookup"><span data-stu-id="2d47f-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="2d47f-109">**DeleteProfile** llama a la función de punto de entrada de todos los servicios de mensajes del perfil con el parámetro  _ulContext_ establecido en MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="2d47f-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="2d47f-110">Las llamadas a las funciones de punto de entrada se producen antes de que los servicios se quiten físicamente del perfil.</span><span class="sxs-lookup"><span data-stu-id="2d47f-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

