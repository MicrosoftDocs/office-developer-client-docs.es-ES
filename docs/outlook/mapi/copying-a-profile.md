---
title: Copiar un perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424731"
---
# <a name="copying-a-profile"></a><span data-ttu-id="9fc0d-103">Copiar un perfil</span><span class="sxs-lookup"><span data-stu-id="9fc0d-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="9fc0d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fc0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fc0d-105">Una forma de crear un perfil es copiar desde un perfil existente y modificar los servicios de mensajes y los proveedores de servicios necesarios.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="9fc0d-106">La copia de un perfil implica el uso de un objeto de administración de perfil, proporcionado por MAPI a través de la [función MAPIAdminProfiles.](mapiadminprofiles.md)</span><span class="sxs-lookup"><span data-stu-id="9fc0d-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="9fc0d-107">**Para copiar un perfil**</span><span class="sxs-lookup"><span data-stu-id="9fc0d-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="9fc0d-108">Llame **a MAPIAdminProfiles** para recuperar un puntero de interfaz **IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="9fc0d-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="9fc0d-109">Llame [a IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="9fc0d-110">Cree una restricción de propiedad con una estructura [SPropertyRestriction](spropertyrestriction.md) para que coincida **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del perfil que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="9fc0d-111">Llame [a IMAPITable::FindRow](imapitable-findrow.md) para buscar la fila adecuada en la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="9fc0d-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="9fc0d-112">Llame [a IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)y pase el valor de **la columna PR_DISPLAY_NAME** como parámetro _lpszOldProfileName._</span><span class="sxs-lookup"><span data-stu-id="9fc0d-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

