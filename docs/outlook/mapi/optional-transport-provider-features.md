---
title: Características opcionales del proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: df38350b049264e7e20ac0bb821c71d93b992d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404305"
---
# <a name="optional-transport-provider-features"></a>Características opcionales del proveedor de transporte

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Entre las características opcionales que los proveedores de transporte pueden implementar se incluyen:
  
- Registrar opciones de mensaje y destinatario específicas del proveedor de transporte.
    
- Mantener un perfil, si es necesario, para almacenar información de configuración y credenciales en el sistema de mensajería.
    
- Realizar cualquier comprobación de las credenciales requeridas por el sistema de mensajería.
    
- Notificación de eventos de soporte técnico para aplicaciones cliente interesadas con [el método IMAPISupport::Notify.](imapisupport-notify.md) 
    
- Mostrar hojas de propiedades de configuración y cuadros de diálogo del asistente para permitir a los usuarios configurar la configuración del proveedor de transporte.
    
- Proporcionar informes de entrega de mensajes a aplicaciones cliente.
    

