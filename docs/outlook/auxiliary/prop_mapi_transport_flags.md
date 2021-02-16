---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y para deshabilitar los elementos de la interfaz de usuario (UI) que la cuenta no admite.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404529"
---
# <a name="prop_mapi_transport_flags"></a>PROP_MAPI_TRANSPORT_FLAGS

Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y para deshabilitar los elementos de la interfaz de usuario (UI) que la cuenta no admite.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2010  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de propiedad:  <br/> |0x20100102  <br/> |
|Acceso:  <br/> |Lectura/escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtenga o establezca esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md) o [IOlkAccount::SetProp,](iolkaccount-setprop.md)respectivamente.
  
Devuelve **MAPIACCT_SEND_ONLY** si la cuenta solo puede enviar mensajes pero no recibir mensajes. En este caso, Outlook deshabilita la interfaz de usuario que no se aplica a este tipo de cuentas (por ejemplo, la interfaz de usuario para **enviar o recibir).**
  
## <a name="see-also"></a>Consulte también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

