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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413307"
---
# <a name="creating-a-profile-by-using-custom-code"></a><span data-ttu-id="67f9a-103">Creación de un perfil mediante código personalizado</span><span class="sxs-lookup"><span data-stu-id="67f9a-103">Creating a Profile by Using Custom Code</span></span>

  
  
<span data-ttu-id="67f9a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67f9a-105">Si decide escribir código para crear un perfil, asegúrese de comprender cómo ordenar entradas de perfil y el tipo y la cantidad de información que se necesita para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="67f9a-105">If you choose to write code to create a profile, make sure that you understand how to order profile entries and the type and amount of information that is needed for each entry.</span></span> <span data-ttu-id="67f9a-106">Las implicaciones de ordenar entradas en un perfil se explican en [Perfiles MAPI](mapi-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="67f9a-106">The implications of ordering entries in a profile is explained in [MAPI Profiles](mapi-profiles.md).</span></span>
  
 <span data-ttu-id="67f9a-107">**Para crear un perfil con código C o C++**</span><span class="sxs-lookup"><span data-stu-id="67f9a-107">**To create a profile with C or C++ code**</span></span>
  
1. <span data-ttu-id="67f9a-108">Lea el archivo de encabezado de cada servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="67f9a-108">Read the header file for each message service.</span></span> <span data-ttu-id="67f9a-109">Comprenda qué propiedades necesitará configurar y qué valores usará.</span><span class="sxs-lookup"><span data-stu-id="67f9a-109">Understand what properties you will need to configure and what values you will use.</span></span>
    
2. <span data-ttu-id="67f9a-110">Llame a [la función MAPIAdminProfiles](mapiadminprofiles.md) para recuperar un puntero de **interfaz IProfAdmin.**</span><span class="sxs-lookup"><span data-stu-id="67f9a-110">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
3. <span data-ttu-id="67f9a-111">Llama [a IProfAdmin::CreateProfile](iprofadmin-createprofile.md) para crear tu perfil.</span><span class="sxs-lookup"><span data-stu-id="67f9a-111">Call [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) to create your profile.</span></span> <span data-ttu-id="67f9a-112">Si desea crear un perfil con los servicios de mensajes enumerados en la sección **[Servicios predeterminados]** de MAPISVC. INF, establezca la marca MAPI_DEFAULT_SERVICE.</span><span class="sxs-lookup"><span data-stu-id="67f9a-112">If you want to create a profile with the message services listed in the **[Default Services]** section of the MAPISVC.INF file, set the MAPI_DEFAULT_SERVICE flag.</span></span> <span data-ttu-id="67f9a-113">Si desea habilitar al usuario para escribir información de configuración, establezca la marca MAPI_DIALOG configuración.</span><span class="sxs-lookup"><span data-stu-id="67f9a-113">If you want to enable the user to enter configuration information, set the MAPI_DIALOG flag.</span></span> <span data-ttu-id="67f9a-114">Asegúrese de establecer esta marca si no toda la información necesaria está disponible a través de MAPISVC. Archivo INF.</span><span class="sxs-lookup"><span data-stu-id="67f9a-114">Make sure that you set this flag if not all of the necessary information is available through the MAPISVC.INF file.</span></span> <span data-ttu-id="67f9a-115">**CreateProfile** llama a la función de punto de entrada de cada servicio de mensajes que se agregará al perfil con MSG_SERVICE_CREATE establecer como el _parámetro ulContext._</span><span class="sxs-lookup"><span data-stu-id="67f9a-115">**CreateProfile** calls the entry point function for each message service to be added to the profile with MSG_SERVICE_CREATE set as the  _ulContext_ parameter.</span></span> 
    
4. <span data-ttu-id="67f9a-116">Llame [a IProfAdmin::AdminServices](iprofadmin-adminservices.md) para obtener un objeto de administración del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="67f9a-116">Call [IProfAdmin::AdminServices](iprofadmin-adminservices.md) to obtain a message service administration object.</span></span> 
    
5. <span data-ttu-id="67f9a-117">Use el objeto de administración del servicio de mensajes para agregar servicios de mensajes al perfil.</span><span class="sxs-lookup"><span data-stu-id="67f9a-117">Use the message service administration object to add message services to the profile.</span></span> <span data-ttu-id="67f9a-118">Para cada servicio de mensajes que desee agregar:</span><span class="sxs-lookup"><span data-stu-id="67f9a-118">For each message service that you want to add:</span></span>
    
1. <span data-ttu-id="67f9a-119">Llame al [método IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) para crear el nuevo servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="67f9a-119">Call the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method to create the new message service.</span></span> 
    
2. <span data-ttu-id="67f9a-120">Llame [a IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), pasando la estructura **MAPIUID** del servicio que acaba de crear y una matriz de valores de propiedad con sus propiedades de configuración.</span><span class="sxs-lookup"><span data-stu-id="67f9a-120">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), passing the **MAPIUID** structure of the service you just created and a property value array with its configuration properties.</span></span> 
    
6. <span data-ttu-id="67f9a-121">Para recuperar el identificador de un servicio recién agregado, que es su propiedad **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), llame a [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para obtener acceso a la tabla de servicio de mensajes y buscar la fila que representa el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="67f9a-121">To retrieve the identifier of a newly added service, which is its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property, call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to access the message service table and search for the row that represents the message service.</span></span> <span data-ttu-id="67f9a-122">La última fila de la tabla representará el servicio de mensajes agregado más recientemente.</span><span class="sxs-lookup"><span data-stu-id="67f9a-122">The last row in the table will represent the most recently added message service.</span></span> 
    
<span data-ttu-id="67f9a-123">Para convertir un nuevo perfil en temporal, llama al [método IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) inmediatamente después de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="67f9a-123">To make a new profile temporary, call the [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) method immediately after you log on.</span></span> <span data-ttu-id="67f9a-124">**DeleteProfile** marcará el nuevo perfil como eliminado mientras lo hace utilizable durante la duración de la sesión.</span><span class="sxs-lookup"><span data-stu-id="67f9a-124">**DeleteProfile** will mark the new profile as deleted while making it usable for the duration of the session.</span></span> <span data-ttu-id="67f9a-125">Dado que no se incluirá en la tabla de perfiles de la sesión, otros clientes no podrán usarlo.</span><span class="sxs-lookup"><span data-stu-id="67f9a-125">Because it will not be included in the session's profile table, other clients will be unable to use it.</span></span> 
  

