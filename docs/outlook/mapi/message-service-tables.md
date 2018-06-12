---
title: Tablas de servicio de mensajes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 81772115fcd4f081718dd560759f6ab93dc7c11c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818406"
---
# <a name="message-service-tables"></a><span data-ttu-id="ae0e4-103">Tablas de servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="ae0e4-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="ae0e4-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae0e4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae0e4-105">La tabla de mensajes de servicio contiene información acerca de los servicios de mensaje en el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="ae0e4-106">Hay una tabla de servicio de mensaje para cada sesión MAPI, implementada por MAPI y usados por las aplicaciones de cliente de propósito especial que proporcionan compatibilidad con la configuración.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="ae0e4-107">La tabla de mensajes de servicio es una tabla estática.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="ae0e4-108">Los clientes de acceso a la tabla de servicio de mensaje llamando al método [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) .</span><span class="sxs-lookup"><span data-stu-id="ae0e4-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="ae0e4-109">Las siguientes propiedades que conforman la columna necesaria establecida en la tabla de servicios de mensaje:</span><span class="sxs-lookup"><span data-stu-id="ae0e4-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ae0e4-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ae0e4-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ae0e4-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ae0e4-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ae0e4-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ae0e4-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="ae0e4-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ae0e4-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ae0e4-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="ae0e4-118">**PR_DISPLAY_NAME** es el nombre que se puede mostrar para el servicio de mensajes y la columna de clave de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="ae0e4-119">**PR_INSTANCE_KEY** sirve la columna de índice para la tabla de caracteres que identifica una fila.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="ae0e4-120">**PR_RESOURCE_FLAGS** describe las capacidades del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="ae0e4-121">**PR_SERVICE_DLL_NAME** es el nombre del archivo DLL que contiene la implementación del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="ae0e4-122">**PR_SERVICE_ENTRY_NAME** es el nombre de la función de punto de entrada del servicio de mensajes que se ajusta al prototipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="ae0e4-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="ae0e4-123">**PR_SERVICE_NAME** es una entrada obligatoria en la sección **[Services]** en MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="ae0e4-124">El valor de esta propiedad nunca cambiará o localizado.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="ae0e4-125">**PR_SERVICE_NAME** puede utilizarse para identificar mediante programación el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="ae0e4-126">**PR_SERVICE_SUPPORT_FILES** es una lista de archivos que debe estar instalado con el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="ae0e4-127">**PR_SERVICE_UID** es un identificador único para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ae0e4-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae0e4-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="ae0e4-128">See also</span></span>



[<span data-ttu-id="ae0e4-129">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="ae0e4-129">MAPI Tables</span></span>](mapi-tables.md)

