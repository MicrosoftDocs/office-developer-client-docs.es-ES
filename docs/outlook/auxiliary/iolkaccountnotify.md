---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: ab24feca84e7049a9800b860c332db52d19cf929
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412502"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Proporciona una devolución de llamada al cliente para realizar cambios en una cuenta.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Suministrado por:  <br/> | Client  <br/> |
|Identificador de interfaz:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Notify](iolkaccountnotify-notify.md) <br/> |Notifica al cliente los cambios en la cuenta especificada.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta interfaz se pasa a [IOlkAccountManager:: Advise](iolkaccountmanager-advise.md) al configurar las notificaciones. 
  
## <a name="see-also"></a>Ver también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

