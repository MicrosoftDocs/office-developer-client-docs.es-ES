---
title: IUnknown IMAPIOfflineNotify
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
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439880"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite Microsoft Outlook 2010 y Microsoft Outlook 2013 para enviar devoluciones de llamada de notificaciones a un cliente.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |Client  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |Envía notificaciones a un cliente sobre los cambios en el estado de conexión.  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente debe implementar esta interfaz y pasar un puntero a ella como miembro en **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** al configurar las devoluciones de llamada mediante **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. Por lo tanto, Outlook 2010 o Outlook 2013 podrán usar esta interfaz para enviar devoluciones de llamada de notificación al cliente. 
  
## <a name="see-also"></a>Ver también



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

