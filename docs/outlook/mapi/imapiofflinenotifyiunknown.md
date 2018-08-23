---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568150"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Es compatible con Microsoft Outlook 2010 y Microsoft Outlook 2013 en el envío de las devoluciones de llamada de notificación a un cliente.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |Envía notificaciones a un cliente acerca de los cambios en el estado de conexión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente debe implementar esta interfaz y pasar un puntero a él como un miembro en **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** al configurar las devoluciones de llamada con **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Posteriormente, Outlook 2010 o Outlook 2013 podrán utilizar esta interfaz para enviar las devoluciones de llamada de notificación al cliente. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

