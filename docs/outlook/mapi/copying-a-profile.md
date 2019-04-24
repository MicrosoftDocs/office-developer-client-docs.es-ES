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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285233"
---
# <a name="copying-a-profile"></a><span data-ttu-id="95bd9-103">Copiar un perfil</span><span class="sxs-lookup"><span data-stu-id="95bd9-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="95bd9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95bd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95bd9-105">Una forma de crear un perfil es copiar a partir de un perfil existente y modificar los servicios de mensajes y los proveedores de servicios necesarios.</span><span class="sxs-lookup"><span data-stu-id="95bd9-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="95bd9-106">La copia de un perfil implica el uso de un objeto de administración de perfiles, proporcionado por MAPI a través de la función [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="95bd9-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="95bd9-107">**Para copiar un perfil**</span><span class="sxs-lookup"><span data-stu-id="95bd9-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="95bd9-108">Llame a **MAPIAdminProfiles** para recuperar un puntero de interfaz **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="95bd9-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="95bd9-109">Llame a [IProfAdmin:: GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="95bd9-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="95bd9-110">Cree una restricción de propiedad con una estructura [SPropertyRestriction](spropertyrestriction.md) para que sea igual a **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del perfil que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="95bd9-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="95bd9-111">Llame al [IMAPITable:: FindRow](imapitable-findrow.md) para localizar la fila adecuada en la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="95bd9-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="95bd9-112">Llame a [IProfAdmin:: CopyProfile](iprofadmin-copyprofile.md)y pase el valor de la columna **PR_DISPLAY_NAME** como el parámetro _lpszOldProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="95bd9-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

