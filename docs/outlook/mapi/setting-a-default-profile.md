---
title: Establecer un perfil predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439817"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="f65ea-103">Establecer un perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="f65ea-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="f65ea-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f65ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f65ea-105">El perfil predeterminado es el perfil que se usa si no se especifica explícitamente uno en la llamada a [MAPILogonEx](mapilogonex.md), estableciendo en su lugar la marca MAPI_USE_DEFAULT usuario.</span><span class="sxs-lookup"><span data-stu-id="f65ea-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="f65ea-106">**Para establecer un perfil predeterminado**</span><span class="sxs-lookup"><span data-stu-id="f65ea-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="f65ea-107">Llame a [la función MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="f65ea-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="f65ea-108">Llame [a IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="f65ea-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="f65ea-109">**SetDefaultProfile** establece la **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para el nuevo perfil predeterminado y quita la configuración del perfil predeterminado anterior.</span><span class="sxs-lookup"><span data-stu-id="f65ea-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

