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
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816646"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="e4cd3-103">Eliminar un perfil</span><span class="sxs-lookup"><span data-stu-id="e4cd3-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="e4cd3-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4cd3-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="e4cd3-105">**Para eliminar un perfil**</span><span class="sxs-lookup"><span data-stu-id="e4cd3-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="e4cd3-106">Llame a [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span><span class="sxs-lookup"><span data-stu-id="e4cd3-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="e4cd3-107">**DeleteProfile** marca el perfil para su eliminación, si se está usando, esperar hasta que ya no está activa para quitarla.</span><span class="sxs-lookup"><span data-stu-id="e4cd3-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="e4cd3-108">El perfil no desaparece realmente hasta que se ha desconectado todos los clientes con una sesión activa.</span><span class="sxs-lookup"><span data-stu-id="e4cd3-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="e4cd3-109">**DeleteProfile** llama a la función de punto de entrada de cada servicio de mensajes en el perfil con el parámetro _ulContext_ establecido en MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="e4cd3-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="e4cd3-110">Las llamadas a las funciones de punto de entrada se producen antes de que los servicios se encuentran físicamente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="e4cd3-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

