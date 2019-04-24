---
title: Buscar un nombre de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336998"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="c4518-103">Buscar un nombre de perfil</span><span class="sxs-lookup"><span data-stu-id="c4518-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="c4518-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4518-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4518-105">A veces, los clientes necesitan encontrar el nombre del perfil que se está usando actualmente para la sesión, el nombre del perfil predeterminado o el nombre de un perfil alternativo instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c4518-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="c4518-106">Hay varias formas de recuperar el nombre de un perfil durante el curso de una sesión.</span><span class="sxs-lookup"><span data-stu-id="c4518-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="c4518-107">Si necesita encontrar el nombre de un perfil que no es necesariamente el que se usa para la sesión, use el primer procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c4518-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="c4518-108">Si necesita buscar el nombre del perfil predeterminado, use el segundo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c4518-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="c4518-109">Si necesita buscar el nombre del perfil actual de la sesión, use el último procedimiento.</span><span class="sxs-lookup"><span data-stu-id="c4518-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="c4518-110">**Para buscar el nombre de un perfil**</span><span class="sxs-lookup"><span data-stu-id="c4518-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="c4518-111">Llame a [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="c4518-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="c4518-112">Llame a [IProfAdmin:: GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="c4518-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="c4518-113">Llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) de la tabla Profile para recuperar todas las filas de la tabla y examinar cada una de ellas para determinar si representa el perfil de destino.</span><span class="sxs-lookup"><span data-stu-id="c4518-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="c4518-114">**Para buscar el nombre del perfil predeterminado**</span><span class="sxs-lookup"><span data-stu-id="c4518-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="c4518-115">Llamar a [MAPIAdminProfiles](mapiadminprofiles.md).</span><span class="sxs-lookup"><span data-stu-id="c4518-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="c4518-116">Llame a [IProfAdmin:: GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfiles.</span><span class="sxs-lookup"><span data-stu-id="c4518-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="c4518-117">Cree una restricción de propiedad con una estructura [SPropertyRestriction](spropertyrestriction.md) para que sea igual a **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) y contenga el valor true.</span><span class="sxs-lookup"><span data-stu-id="c4518-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="c4518-118">Llame al [IMAPITable:: FindRow](imapitable-findrow.md) para localizar la fila en la tabla de perfiles que representa el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c4518-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="c4518-119">La columna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contiene el nombre del perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c4518-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="c4518-120">**Para buscar el nombre del perfil actual**</span><span class="sxs-lookup"><span data-stu-id="c4518-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="c4518-121">Para buscar el nombre del perfil actual, siga uno de estos pasos:</span><span class="sxs-lookup"><span data-stu-id="c4518-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="c4518-122">SuPoniendo que tiene la estructura [MAPIUID](mapiuid.md) que representa una de las secciones del perfil actual, pásela en el parámetro _lpUID_ a [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="c4518-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="c4518-123">Recupere la propiedad **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) de la sección de perfil mediante su método [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="c4518-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="c4518-124">Llame a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para tener acceso a la tabla de estado y busque la fila que tiene su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) establecida en MAPI_SUBSYSTEM.</span><span class="sxs-lookup"><span data-stu-id="c4518-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="c4518-125">La columna **PR_DISPLAY_NAME** de esta fila es el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="c4518-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="c4518-126">No use la tabla de estado durante el inicio porque bloquea una aplicación hasta que la cola MAPI haya finalizado la inicialización de todos los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="c4518-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="c4518-127">Esto puede afectar al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c4518-127">This can degrade your performance.</span></span> 
    

