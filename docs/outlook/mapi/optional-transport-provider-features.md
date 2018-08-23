---
title: Características del proveedor de transporte opcionales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b55e6518ee1f3f59ef0459b3aeb68461f00a7ab3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566827"
---
# <a name="optional-transport-provider-features"></a>Características del proveedor de transporte opcionales

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las características opcionales que pueden implementar proveedores de transporte incluyen:
  
- Registrar el mensaje y el destinatarios opciones específicas del proveedor de transporte.
    
- Mantenimiento de un perfil, si es necesario, para almacenar las credenciales para el sistema de mensajería e información de configuración.
    
- Realización de cualquier comprobación de credenciales requeridos por el sistema de mensajería.
    
- Admiten la notificación de eventos para las aplicaciones cliente interesado con el método [IMAPISupport::Notify](imapisupport-notify.md) . 
    
- Para mostrar las hojas de propiedades de configuración y cuadros de diálogo Asistente para habilitar a los usuarios establecer la configuración del proveedor de transporte.
    
- Proporcionar informes de entrega de mensajes a las aplicaciones cliente.
    

