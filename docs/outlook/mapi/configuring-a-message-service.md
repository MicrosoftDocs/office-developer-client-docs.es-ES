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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335115"
---
# <a name="configuring-a-message-service"></a>Configuración de un servicio de mensajes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 **Para configurar todos los proveedores de servicios en un servicio de mensajes**
  
- Llamar a [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Si todos los datos necesarios para la configuración están disponibles mediante programación, puede elegir si desea mostrar una interfaz de usuario. Sin embargo, si parte de la información de uno o más proveedores no está disponible, asegúrese de establecer la marca SERVICE_UI_ALLOWED o SERVICE_UI_ALWAYS. Suprimir una interfaz de usuario cuando los datos de configuración necesarios no están disponibles da como resultado un servicio de mensajes no configurado.
    
 **Para configurar un proveedor de servicios único en un servicio de mensajes**
  
1. Llame a [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) para tener acceso al objeto de estado del proveedor de servicios. 
    
2. Llame a [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para mostrar la hoja de propiedades del proveedor de servicios. 
    
Para obtener más información acerca del uso de objetos de estado, consulte [tabla de estado y objetos de estado](status-table-and-status-objects.md).
  

