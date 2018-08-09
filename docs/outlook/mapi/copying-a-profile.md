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
ms.openlocfilehash: 77c7853c07830804aaa044f08078d95785bcfda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816581"
---
# <a name="copying-a-profile"></a><span data-ttu-id="16b65-103">Copiar un perfil</span><span class="sxs-lookup"><span data-stu-id="16b65-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="16b65-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16b65-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16b65-105">Es una forma de crear un perfil copiar de un perfil existente y modifique los servicios de mensajes es necesario y proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="16b65-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="16b65-106">Copiar un perfil de implica el uso de un objeto de administración de perfiles, proporcionado por MAPI a través de la función [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="16b65-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="16b65-107">**Para copiar un perfil**</span><span class="sxs-lookup"><span data-stu-id="16b65-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="16b65-108">Llame a **MAPIAdminProfiles** para recuperar un puntero de interfaz **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="16b65-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="16b65-109">Llame a [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="16b65-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="16b65-110">Crear una restricción de propiedad con una estructura de [SPropertyRestriction](spropertyrestriction.md) para que coincida con **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre del perfil que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="16b65-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="16b65-111">Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para localizar la fila apropiada en la tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="16b65-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="16b65-112">Llame a [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), pasando el valor de la columna **PR_DISPLAY_NAME** como el parámetro _lpszOldProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="16b65-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

