---
title: Características del proveedor de transporte opcional
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: fd685e5bc67a3cb0785d9102e94c11ea921f07ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818447"
---
# <a name="optional-transport-provider-features"></a>Características del proveedor de transporte opcional

  
  
**Se aplica a**: Outlook 
  
Las características opcionales que pueden implementar proveedores de transporte incluyen:
  
- Registrar el mensaje y el destinatarios opciones específicas del proveedor de transporte.
    
- Mantenimiento de un perfil, si es necesario, para almacenar las credenciales para el sistema de mensajería e información de configuración.
    
- Realización de cualquier comprobación de credenciales requeridos por el sistema de mensajería.
    
- Admiten la notificación de eventos para las aplicaciones cliente interesado con el método [IMAPISupport::Notify](imapisupport-notify.md) . 
    
- Para mostrar las hojas de propiedades de configuración y cuadros de diálogo Asistente para habilitar a los usuarios establecer la configuración del proveedor de transporte.
    
- Proporcionar informes de entrega de mensajes a las aplicaciones cliente.
    

