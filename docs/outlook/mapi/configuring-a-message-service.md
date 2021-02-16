---
title: Configuración de un servicio de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434511"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="5f2e9-103">Configuración de un servicio de mensajes</span><span class="sxs-lookup"><span data-stu-id="5f2e9-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="5f2e9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f2e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5f2e9-105">**Para configurar todos los proveedores de servicios en un servicio de mensajes**</span><span class="sxs-lookup"><span data-stu-id="5f2e9-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="5f2e9-106">Llame [a IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="5f2e9-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="5f2e9-107">Si todos los datos necesarios para la configuración están disponibles mediante programación, puede elegir si desea mostrar o no una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5f2e9-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="5f2e9-108">Sin embargo, si parte de la información de uno o más proveedores no está disponible, asegúrese de establecer la marca SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS proveedor.</span><span class="sxs-lookup"><span data-stu-id="5f2e9-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="5f2e9-109">La supresión de una interfaz de usuario cuando los datos de configuración necesarios no están disponibles da como resultado un servicio de mensajes no configurado.</span><span class="sxs-lookup"><span data-stu-id="5f2e9-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="5f2e9-110">**Para configurar un único proveedor de servicios en un servicio de mensajes**</span><span class="sxs-lookup"><span data-stu-id="5f2e9-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="5f2e9-111">Llame [a IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso al objeto de estado del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="5f2e9-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="5f2e9-112">Llame [a IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="5f2e9-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="5f2e9-113">Para obtener más información acerca del uso de objetos de estado, vea [Tabla de estado y Objetos de estado](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5f2e9-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

