---
title: Información sobre la API de estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410486"
---
# <a name="about-the-offline-state-api"></a>Información sobre la API de estado sin conexión

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de estado sin conexión admite devoluciones de llamada que indican cambios en el estado de conexión de un usuario en Microsoft Outlook 2013 y Microsoft Outlook 2010, por ejemplo, desde estar en línea en Outlook 2013 o Outlook 2010 hasta estar sin conexión. La API usa un objeto sin conexión global en Outlook 2013 o Outlook 2010 para realizar un seguimiento de estos cambios para un perfil de cuenta de usuario determinado. La notificación es la única forma compatible de devolución de llamada. Como clientes de esta API, los proveedores de correo que desean recibir una notificación de estos cambios de estado de conexión hacen lo siguiente:
  
1. Implementar **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Abra un objeto sin conexión existente para un perfil específico mediante **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Determinar si el objeto tiene la capacidad de proporcionar notificaciones en línea o sin conexión mediante **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Registre el objeto para notificaciones en línea o sin conexión **[con IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Los proveedores de correo ahora pueden recibir notificaciones que Outlook 2013 o Outlook 2010 envían **mediante IMAPIOfflineNotify**. 
    
5. Al cerrar, quite el registro de las notificaciones en línea y sin conexión con **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> En general, Outlook 2013 y Outlook 2010 pueden notificar a un cliente los cambios en línea o sin conexión, así como otros cambios, pero la API de estado sin conexión solo admite notificaciones para cambios en línea o sin conexión. El cliente debe omitir todas las demás notificaciones. Para obtener más información, **[vea IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** y **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Para obtener un ejemplo de un cliente que usa la API de estado sin conexión, vea Acerca del [complemento de estado sin conexión de ejemplo.](about-the-sample-offline-state-add-in.md) El complemento de estado sin conexión de ejemplo es un complemento COM que usa la API de estado sin conexión para supervisar y cambiar el estado de conexión.
  
Esta API proporciona lo siguiente:
  
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
    

