---
title: Configuración de un perfil predeterminado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820634"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="9e19a-103">Configuración de un perfil predeterminado</span><span class="sxs-lookup"><span data-stu-id="9e19a-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="9e19a-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e19a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e19a-105">El perfil predeterminado es el perfil que se usa si no especificar de forma explícita en la llamada a [MAPILogonEx](mapilogonex.md), en su lugar, establecer el indicador MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="9e19a-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="9e19a-106">**Para establecer un perfil predeterminado**</span><span class="sxs-lookup"><span data-stu-id="9e19a-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="9e19a-107">Llame a la función [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="9e19a-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="9e19a-108">Llame a [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="9e19a-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="9e19a-109">**SetDefaultProfile** establece la propiedad **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) para el nuevo perfil predeterminado y se quita la configuración para el perfil predeterminado anterior.</span><span class="sxs-lookup"><span data-stu-id="9e19a-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

