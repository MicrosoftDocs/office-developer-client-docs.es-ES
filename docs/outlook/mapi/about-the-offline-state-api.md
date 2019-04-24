---
title: Información sobre la API de estado sin conexión
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321794"
---
# <a name="about-the-offline-state-api"></a>Información sobre la API de estado sin conexión

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de estado sin conexión admite las devoluciones de llamada que indican cambios en el estado de conexión de un usuario en Microsoft Outlook 2013 y Microsoft Outlook 2010 (por ejemplo, que están en línea en Outlook 2013 o en Outlook 2010 para estar sin conexión). La API usa un objeto global sin conexión en Outlook 2013 o en Outlook 2010 para realizar un seguimiento de estos cambios en un perfil de cuenta de usuario determinado. Notification es la única forma admitida de devolución de llamada. Como clientes de esta API, los proveedores de correo que quieran recibir una notificación de los cambios en el estado de conexión hacen lo siguiente:
  
1. Implementar **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Abrir un objeto sin conexión existente para un perfil específico mediante **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. DeTermine si el objeto tiene la capacidad de suministrar notificaciones en línea o sin conexión con **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Registre el objeto para las notificaciones en línea o sin conexión mediante **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. Los proveedores de correo ahora pueden recibir notificaciones que Outlook 2013 o Outlook 2010 envíen mediante **IMAPIOfflineNotify**. 
    
5. Al cerrar, quitar el registro de las notificaciones en línea y sin conexión con **[IMAPIOfflineMgr:: Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> En general, Outlook 2013 y Outlook 2010 pueden notificar a un cliente los cambios en línea/sin conexión, así como otros cambios, pero la API de estado sin conexión solo admite notificaciones para cambios en línea o sin conexión. El cliente debe omitir el resto de las notificaciones. Para obtener más información, vea **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** y **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Para ver un ejemplo de un cliente que usa la API de estado sin conexión, consulte [acerca del complemento de estado sin conexión de muestra](about-the-sample-offline-state-add-in.md). El complemento de estado sin conexión de muestra es un complemento COM que usa la API de estado sin conexión para supervisar y cambiar el estado de conexión.
  
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
    

