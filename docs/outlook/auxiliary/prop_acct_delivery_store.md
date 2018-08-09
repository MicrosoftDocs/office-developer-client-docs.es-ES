---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816310"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.
  
## <a name="quick-info"></a>Información rápida

Vea [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0018  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de la propiedad:  <br/> |0x00180102  <br/> |
|Access:  <br/> |Es de lectura y escritura.  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtener o establecer esta propiedad mediante [IOlkAccount::GetProp](iolkaccount-getprop.md) o [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.
  
Uno de los efectos secundarios de la configuración de un almacén como el almacén de entrega predeterminado para una cuenta es que, al iniciar Outlook, Outlook crea las carpetas de búsqueda de ese almacén si no está ya no existe y el almacenamiento en la barra Tareas pendientes de lista.
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

