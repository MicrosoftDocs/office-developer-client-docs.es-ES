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
# <a name="configuring-a-message-service"></a>Configuración de un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para configurar todos los proveedores de servicios en un servicio de mensajes**
  
- Llame [a IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Si todos los datos necesarios para la configuración están disponibles mediante programación, puede elegir si desea mostrar o no una interfaz de usuario. Sin embargo, si parte de la información de uno o varios proveedores no está disponible, asegúrese de establecer la marca SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS proveedor. La supresión de una interfaz de usuario cuando los datos de configuración necesarios no están disponibles da como resultado un servicio de mensajes no configurado.
    
 **Para configurar un único proveedor de servicios en un servicio de mensajes**
  
1. Llame [a IMAPISession::GetStatusTable para](imapisession-getstatustable.md) obtener acceso al objeto de estado del proveedor de servicios. 
    
2. Llame [a IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades del proveedor de servicios. 
    
Para obtener más información acerca del uso de objetos de estado, vea [Tabla de estado y Objetos de estado](status-table-and-status-objects.md).
  

