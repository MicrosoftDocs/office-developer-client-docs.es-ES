---
title: PROP_MAPI_TRANSPORT_FLAGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 12cfe096-6882-c0be-b248-87567cb71e83
description: Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y deshabilitar los elementos de la interfaz de usuario (UI) que no son compatibles con la cuenta.
ms.openlocfilehash: 707306c3bfbeebdd18f82bacfc121274be08aa50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326484"
---
# <a name="propmapitransportflags"></a>PROP_MAPI_TRANSPORT_FLAGS

Representa la configuración de transporte que Outlook usa para determinar las tareas de sincronización necesarias y deshabilitar los elementos de la interfaz de usuario (UI) que no son compatibles con la cuenta.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2010  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de propiedad:  <br/> |0x20100102  <br/> |
|Al  <br/> |Lectura y escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtenga o establezca esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md) o [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivamente.
  
Devuelve **MAPIACCT_SEND_ONLY** si la cuenta solo puede enviar mensajes, pero no puede recibirlos. En este caso, Outlook deshabilita la interfaz de usuario que no se aplica a este tipo de cuentas (por ejemplo, la interfaz de usuario para el **envío o recepción**).
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

