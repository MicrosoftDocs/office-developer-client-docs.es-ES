---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327674"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Representa el identificador de entrada del almacén de entrega predeterminado para la cuenta.
  
## <a name="quick-info"></a>Información rápida

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0018  <br/> |
|Tipo de propiedad:  <br/> |PT_BINARY  <br/> |
|Etiqueta de propiedad:  <br/> |0x00180102  <br/> |
|Al  <br/> |Lectura y escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

Obtenga o establezca esta propiedad mediante [IOlkAccount:: GetProp](iolkaccount-getprop.md) o [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivamente.
  
Uno de los efectos secundarios de establecer un almacén como el almacén de entrega predeterminado para una cuenta es que al iniciar Outlook, Outlook crea carpetas de búsqueda para ese almacén si todavía no existen y muestra el almacén en la barra tareas pendientes.
  
## <a name="see-also"></a>Vea también

- [Acerca de la API de administración de cuenta](about-the-account-management-api.md)
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

