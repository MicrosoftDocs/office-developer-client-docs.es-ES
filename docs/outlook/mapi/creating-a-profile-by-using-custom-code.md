---
title: Creación de un perfil mediante código personalizado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335796"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="533e6-103">Creación de un perfil mediante código personalizado</span><span class="sxs-lookup"><span data-stu-id="533e6-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="533e6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="533e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="533e6-105">Si elige escribir código para crear un perfil, asegúrese de que comprende cómo ordenar las entradas de perfil y el tipo y la cantidad de información necesaria para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="533e6-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="533e6-106">Las implicaciones de las entradas de ordenación en un perfil se explican en los [perfiles MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="533e6-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="533e6-107">**Para crear un perfil con código C o C++**</span><span class="sxs-lookup"><span data-stu-id="533e6-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="533e6-108">Lea el archivo de encabezado para cada servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="533e6-108">Read the header file for each message service.</span></span> <span data-ttu-id="533e6-109">Comprenda qué propiedades tendrá que configurar y qué valores va a usar.</span><span class="sxs-lookup"><span data-stu-id="533e6-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="533e6-110">Llame a la función [MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de interfaz **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="533e6-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="533e6-111">Llame a [IProfAdmin:: CreateProfile](iprofadmin-createprofile.md) para crear su perfil.</span><span class="sxs-lookup"><span data-stu-id="533e6-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="533e6-112">Si desea crear un perfil con los servicios de mensajes enumerados en la sección **[default Services]** del MAPISVC. INF, establezca la marca MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="533e6-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="533e6-113">Si desea permitir que el usuario escriba información de configuración, establezca la marca MAPI_DIALOG.</span><span class="sxs-lookup"><span data-stu-id="533e6-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="533e6-114">Asegúrese de establecer esta marca si no toda la información necesaria está disponible a través del MAPISVC. Archivo INF.</span><span class="sxs-lookup"><span data-stu-id="533e6-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="533e6-115">**CreateProfile** llama a la función de punto de entrada para que cada servicio de mensajes se agregue al perfil con MSG_SERVICE_CREATE establecido como el parámetro _ulContext_ .</span><span class="sxs-lookup"><span data-stu-id="533e6-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="533e6-116">Llame a [IProfAdmin:: AdminServices](iprofadmin-adminservices.md) para obtener un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="533e6-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="533e6-117">Use el objeto de administración del servicio de mensajes para agregar servicios de mensajes al perfil.</span><span class="sxs-lookup"><span data-stu-id="533e6-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="533e6-118">Para cada servicio de mensajes que desee agregar:</span><span class="sxs-lookup"><span data-stu-id="533e6-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="533e6-119">Llame al método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) para crear el nuevo servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="533e6-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="533e6-120">Llame a [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), pasando la estructura **MAPIUID** del servicio que acaba de crear y una matriz de valores de propiedad con sus propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="533e6-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="533e6-121">Para recuperar el identificador de un servicio recién agregado, que es su propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), llame a [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener acceso a la tabla de servicio de mensajes y busque la fila que representa el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="533e6-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="533e6-122">La última fila de la tabla representará el servicio de mensajes que se ha agregado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="533e6-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="533e6-123">Para crear un nuevo perfil temporal, llame al método [IProfAdmin::D eleteprofile](iprofadmin-deleteprofile.md) inmediatamente después de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="533e6-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="533e6-124">**DeleteProfile** marcará el nuevo perfil como eliminado mientras se puede usar durante la duración de la sesión.</span><span class="sxs-lookup"><span data-stu-id="533e6-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="533e6-125">Como no se incluirá en la tabla de perfiles de la sesión, otros clientes no podrán usarla.</span><span class="sxs-lookup"><span data-stu-id="533e6-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

