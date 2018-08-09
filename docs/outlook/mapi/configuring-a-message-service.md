---
title: Configurar un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: fd87d169cd5131c6e1c8ca45a35dded96a295c57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816549"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="56bd2-103">Configurar un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="56bd2-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="56bd2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="56bd2-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="56bd2-105">**Para configurar todos los proveedores de servicio en un servicio de mensajes**</span><span class="sxs-lookup"><span data-stu-id="56bd2-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="56bd2-106">Llame a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="56bd2-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="56bd2-107">Si todos los datos necesarios para la configuración está disponible mediante programación, puede elegir si desea o no mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="56bd2-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="56bd2-108">Sin embargo, si parte de la información para uno o más proveedores no está disponible, asegúrese de que se establece la marca SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="56bd2-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="56bd2-109">Supresión de una interfaz de usuario cuando los datos de configuración necesarias resultados no está disponible en un servicio de mensajes no configurado.</span><span class="sxs-lookup"><span data-stu-id="56bd2-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="56bd2-110">**Para configurar un proveedor de servicio único en un servicio de mensajes**</span><span class="sxs-lookup"><span data-stu-id="56bd2-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="56bd2-111">Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a objetos de estado de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="56bd2-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="56bd2-112">Llame a [SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades de un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="56bd2-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="56bd2-113">Para obtener más información acerca del uso de objetos de estado, vea la [tabla de estado y objetos de estado](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="56bd2-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

