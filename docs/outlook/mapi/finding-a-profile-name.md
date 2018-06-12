---
title: Buscar un nombre de perfil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 332b78bcebbcd54de43376553ec4aea386c1c359
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816813"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="aa228-103">Buscar un nombre de perfil</span><span class="sxs-lookup"><span data-stu-id="aa228-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="aa228-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa228-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa228-105">A veces, los clientes necesitan buscar el nombre del perfil se utiliza actualmente para la sesión, el nombre del perfil predeterminado o el nombre de un perfil alternativo instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="aa228-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="aa228-106">Hay varias formas de recuperar el nombre de un perfil durante el transcurso de una sesión.</span><span class="sxs-lookup"><span data-stu-id="aa228-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="aa228-107">Si necesita buscar el nombre de un perfil que no es necesariamente la que se utiliza para la sesión, use el primer procedimiento.</span><span class="sxs-lookup"><span data-stu-id="aa228-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="aa228-108">Si necesita buscar el nombre del perfil predeterminado, use el segundo procedimiento.</span><span class="sxs-lookup"><span data-stu-id="aa228-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="aa228-109">Si necesita encontrar el nombre del perfil actual de la sesión, use el último procedimiento.</span><span class="sxs-lookup"><span data-stu-id="aa228-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="aa228-110">**Para buscar el nombre de cualquier perfil**</span><span class="sxs-lookup"><span data-stu-id="aa228-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="aa228-111">Llame a [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="aa228-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="aa228-112">Llame a [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="aa228-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="aa228-113">Llamar al método [IMAPITable:: QueryRows](imapitable-queryrows.md) de la tabla de perfil para recuperar todas las filas en la tabla y examinar cada uno de ellos para determinar si representa el perfil de destino.</span><span class="sxs-lookup"><span data-stu-id="aa228-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="aa228-114">**Para buscar el nombre del perfil predeterminado**</span><span class="sxs-lookup"><span data-stu-id="aa228-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="aa228-115">Llame a [MAPIAdminProfiles](mapiadminprofiles.md).</span><span class="sxs-lookup"><span data-stu-id="aa228-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="aa228-116">Llame a [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) para obtener acceso a la tabla de perfil.</span><span class="sxs-lookup"><span data-stu-id="aa228-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="aa228-117">Crear una restricción de propiedad con una estructura de [SPropertyRestriction](spropertyrestriction.md) para que coincida con **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) con el valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="aa228-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="aa228-118">Llamar a [IMAPITable:: FindRow](imapitable-findrow.md) para localizar la fila en la tabla de perfil que representa el perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aa228-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="aa228-119">La columna **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contiene el nombre del perfil predeterminado.</span><span class="sxs-lookup"><span data-stu-id="aa228-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="aa228-120">**Para buscar el nombre del perfil actual**</span><span class="sxs-lookup"><span data-stu-id="aa228-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="aa228-121">Para buscar el nombre del perfil actual, siga uno de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="aa228-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="aa228-122">Suponiendo que tiene la estructura [MAPIUID](mapiuid.md) que representa una de las secciones del perfil actual, páselo en el parámetro _lpUID_ a [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="aa228-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="aa228-123">Recuperar la propiedad de **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) de la sección de perfil mediante el método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="aa228-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="aa228-124">Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acceder a la tabla de estado y busque la fila que tiene su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) que se establece en MAPI_SUBSYSTEM.</span><span class="sxs-lookup"><span data-stu-id="aa228-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="aa228-125">La columna **PR_DISPLAY_NAME** para esta fila es el nombre del perfil.</span><span class="sxs-lookup"><span data-stu-id="aa228-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="aa228-126">No use la tabla de estado durante el inicio debido a que se bloquea una aplicación hasta que la cola MAPI ha terminado de inicializar todos los proveedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="aa228-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="aa228-127">Esto puede afectar negativamente al rendimiento de su.</span><span class="sxs-lookup"><span data-stu-id="aa228-127">This can degrade your performance.</span></span> 
    

