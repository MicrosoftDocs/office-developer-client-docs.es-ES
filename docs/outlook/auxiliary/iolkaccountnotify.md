---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: f4b57ad1062df9aa1809e8eb422a2c983adcac4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816242"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Proporciona una devolución de llamada al cliente para que los cambios a una cuenta.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Suministrado por:  <br/> | Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |Notifica al cliente de los cambios realizados en la cuenta especificada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz se pasa al [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) al configurar las notificaciones. 
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

