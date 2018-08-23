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
ms.openlocfilehash: 2b170037bc51a7848154c12acbfe700a0142ef8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564111"
---
# <a name="configuring-a-message-service"></a>Configurar un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para configurar todos los proveedores de servicio en un servicio de mensajes**
  
- Llame a [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Si todos los datos necesarios para la configuración está disponible mediante programación, puede elegir si desea o no mostrar una interfaz de usuario. Sin embargo, si parte de la información para uno o más proveedores no está disponible, asegúrese de que se establece la marca SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS. Supresión de una interfaz de usuario cuando los datos de configuración necesarias resultados no está disponible en un servicio de mensajes no configurado.
    
 **Para configurar un proveedor de servicio único en un servicio de mensajes**
  
1. Llame a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para obtener acceso a objetos de estado de un proveedor de servicios. 
    
2. Llame a [SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades de un proveedor de servicios. 
    
Para obtener más información acerca del uso de objetos de estado, vea la [tabla de estado y objetos de estado](status-table-and-status-objects.md).
  

