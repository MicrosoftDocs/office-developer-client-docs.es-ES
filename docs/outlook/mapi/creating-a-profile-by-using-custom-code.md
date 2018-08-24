---
title: Crear un perfil con código personalizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c14d58e8a03633615798b50b256b9cc54fcc4f4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594736"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="c3a6d-103">Crear un perfil con código personalizado</span><span class="sxs-lookup"><span data-stu-id="c3a6d-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="c3a6d-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3a6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3a6d-105">Si opta por escribir código para crear un perfil, asegúrese de que comprende cómo ordenar las entradas del perfil y el tipo y la cantidad de información que se necesita para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="c3a6d-106">Las implicaciones de las entradas de ordenación en un perfil se explica en [Perfiles de MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="c3a6d-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="c3a6d-107">**Para crear un perfil con el código de C o C++**</span><span class="sxs-lookup"><span data-stu-id="c3a6d-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="c3a6d-108">Leer el archivo de encabezado para cada servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-108">Read the header file for each message service.</span></span> <span data-ttu-id="c3a6d-109">Comprender qué propiedades debe configurar y qué valores se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="c3a6d-110">Llame a la función [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="c3a6d-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="c3a6d-111">Llame a [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) para crear un perfil.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="c3a6d-112">Si desea crear un perfil con los servicios de mensaje que aparecen en la sección **[Services predeterminado]** de la MAPISVC. Archivo INF, establecer la marca MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="c3a6d-113">Si desea habilitar al usuario para escribir información de configuración, establecer la marca MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="c3a6d-114">Asegúrese de que se establezca esta marca si no está disponible a través de la MAPISVC toda la información necesaria. Archivo INF.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="c3a6d-115">**CreateProfile** llama a la función de punto de entrada para cada servicio de mensajes que se agregará al perfil con MSG_SERVICE_CREATE establecido como el parámetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="c3a6d-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="c3a6d-116">Llame a [IProfAdmin::AdminServices](iprofadmin-adminservices.md) para obtener un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="c3a6d-117">Use el objeto de administración del servicio de mensajes para agregar servicios de mensajes para el perfil.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="c3a6d-118">Para cada servicio de mensajes que desea agregar:</span><span class="sxs-lookup"><span data-stu-id="c3a6d-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="c3a6d-119">Llame al método [IMsgServiceAdmin::](imsgserviceadmin-createmsgservice.md) para crear el nuevo servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="c3a6d-120">Llame a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), pasando la estructura **MAPIUID** del servicio que acaba de crear y una matriz de valores de propiedad con sus propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="c3a6d-121">Para recuperar el identificador de un servicio recién agregado, que es su propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), llame a [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener acceso a la tabla de mensajes de servicio y la búsqueda de la fila que representa el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="c3a6d-122">La última fila de la tabla representa el servicio de mensajes agregado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="c3a6d-123">Para hacer que un nuevo perfil temporal, llame al método [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) inmediatamente después de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="c3a6d-124">**DeleteProfile** marcará el nuevo perfil como eliminada mientras realiza utilizable para la duración de la sesión.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="c3a6d-125">Debido a que no se incluirá en la tabla de perfiles de la sesión, otros clientes podrán utilizarlo.</span><span class="sxs-lookup"><span data-stu-id="c3a6d-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

