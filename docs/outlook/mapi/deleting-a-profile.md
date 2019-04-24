---
title: Eliminación de un perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316831"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="e6a84-103">Eliminación de un perfil</span><span class="sxs-lookup"><span data-stu-id="e6a84-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="e6a84-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6a84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e6a84-105">**Para eliminar un perfil**</span><span class="sxs-lookup"><span data-stu-id="e6a84-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="e6a84-106">Llamar a [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="e6a84-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="e6a84-107">**DeleteProfile** marca el perfil para su eliminación si se está usando actualmente, esperando hasta que ya no esté activo para quitarlo.</span><span class="sxs-lookup"><span data-stu-id="e6a84-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="e6a84-108">En realidad, el perfil no desaparecerá hasta que se desconecte todos los clientes con una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="e6a84-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="e6a84-109">**DeleteProfile** llama a la función de punto de entrada de cada servicio de mensajes en el perfil con el parámetro _ULCONTEXT_ establecido en MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="e6a84-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="e6a84-110">Las llamadas a las funciones de punto de entrada ocurren antes de que los servicios se hayan quitado físicamente del perfil.</span><span class="sxs-lookup"><span data-stu-id="e6a84-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

