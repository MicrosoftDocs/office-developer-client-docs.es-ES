---
title: Información sobre la API de estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816377"
---
# <a name="about-the-offline-state-api"></a>Información sobre la API de estado sin conexión

  
  
**Hace referencia a**: Outlook 
  
La API de estado sin conexión admite las devoluciones de llamada que indica los cambios en el estado de conexión de un usuario en Microsoft Outlook 2013 y Microsoft Outlook 2010: por ejemplo, desde la que se está en línea en Outlook 2013 o Outlook 2010 para que se está sin conexión. La API usa un objeto global sin conexión en Outlook 2013 o Outlook 2010 para realizar un seguimiento de dichos cambios para un perfil de cuenta de usuario determinado. Notificación es la única forma compatible de devolución de llamada. Como los clientes de esta API, los proveedores de correo que desean recibir una notificación de estos cambios de estado de conexión, haga lo siguiente:
  
1. Implemente **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Abrir un objeto sin conexión existente para un perfil específico mediante **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Determinar si el objeto tiene la capacidad de proporcionar notificaciones en línea o sin conexión con **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Registre el objeto para las notificaciones en línea o sin conexión con **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Proveedores de correo ahora pueden recibir notificaciones de que Outlook 2013 o Outlook 2010 enviar utilizando **IMAPIOfflineNotify**. 
    
5. En el cierre, quite el registro para las notificaciones de en línea y sin conexión mediante **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> En general, Outlook 2013 y Outlook 2010 pueden notificar a un cliente de los cambios en línea o sin conexión, así como otros cambios, pero la API de estado sin conexión admite solamente las notificaciones de cambios en línea o sin conexión. El cliente debe omitir todas las notificaciones de otras. Para obtener más información, vea **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** y **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Para obtener un ejemplo de un cliente que usa la API de estado sin conexión, vea [Agregar en sobre el ejemplo de estado no conectado](about-the-sample-offline-state-add-in.md). El complemento de estado sin conexión de ejemplo es un complemento COM que usa la API de estado sin conexión para supervisar y cambiar el estado de conexión.
  
Esta API ofrece lo siguiente:
  
Definiciones:
  
- [Constantes MAPI](mapi-constants.md)
    
Tipos de datos:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Funciones:
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Interfaces:
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

