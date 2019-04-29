---
title: Tablas de servicio de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422498"
---
# <a name="message-service-tables"></a><span data-ttu-id="03a14-103">Tablas de servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="03a14-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="03a14-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03a14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03a14-105">La tabla servicio de mensajes contiene información sobre los servicios de mensajes en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="03a14-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="03a14-106">Hay una tabla de servicio de mensajes para cada sesión MAPI, implementada por MAPI y utilizada por aplicaciones cliente de uso especial que proporcionan compatibilidad con la configuración.</span><span class="sxs-lookup"><span data-stu-id="03a14-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="03a14-107">La tabla de servicio de mensajes es una tabla estática.</span><span class="sxs-lookup"><span data-stu-id="03a14-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="03a14-108">Los clientes tienen acceso a la tabla de servicio de mensajes llamando al método [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) .</span><span class="sxs-lookup"><span data-stu-id="03a14-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="03a14-109">Las siguientes propiedades conforman la columna obligatoria que se establece en la tabla de servicio de mensajes:</span><span class="sxs-lookup"><span data-stu-id="03a14-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03a14-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03a14-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="03a14-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03a14-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="03a14-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03a14-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="03a14-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="03a14-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="03a14-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="03a14-118">**PR_DISPLAY_NAME** es el nombre que se puede mostrar para el servicio de mensajes y la columna de criterio de ordenación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="03a14-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="03a14-119">**PR_INSTANCE_KEY** sirve como columna de índice de la tabla, identificando de forma única una fila.</span><span class="sxs-lookup"><span data-stu-id="03a14-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="03a14-120">**PR_RESOURCE_FLAGS** describe las capacidades del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="03a14-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="03a14-121">**PR_SERVICE_DLL_NAME** es el nombre de la dll que contiene la implementación del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="03a14-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="03a14-122">**PR_SERVICE_ENTRY_NAME** es el nombre de la función de punto de entrada del servicio de mensajería que se ajusta al prototipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="03a14-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="03a14-123">**PR_SERVICE_NAME** es una entrada obligatoria en la sección **[Services]** del archivo MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="03a14-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="03a14-124">El valor de esta propiedad nunca se cambiará ni se localizará.</span><span class="sxs-lookup"><span data-stu-id="03a14-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="03a14-125">**PR_SERVICE_NAME** puede usarse para identificar el servicio de mensajes mediante programación.</span><span class="sxs-lookup"><span data-stu-id="03a14-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="03a14-126">**PR_SERVICE_SUPPORT_FILES** es una lista de los archivos que se deben instalar con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="03a14-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="03a14-127">**PR_SERVICE_UID** es un identificador único para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="03a14-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="03a14-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="03a14-128">See also</span></span>



[<span data-ttu-id="03a14-129">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="03a14-129">MAPI Tables</span></span>](mapi-tables.md)

