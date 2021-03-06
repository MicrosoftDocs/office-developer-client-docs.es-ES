---
title: Administrar un proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416541"
---
# <a name="handling-a-transport-provider"></a>Administrar un proveedor de transporte
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes se comunican con proveedores de transporte a través de objetos de estado proporcionados por proveedores de transporte y la cola MAPI. Los clientes obtienen acceso a objetos de estado [llamando a IMAPISession::GetStatusTable para](imapisession-getstatustable.md) recuperar la tabla de estado. Los objetos status implementan la interfaz [IMAPIStatus : IMAPIProp,](imapistatusimapiprop.md) que tiene métodos para configurar proveedores, vaciar colas de mensajes entrantes y salientes, establecer contraseñas y validación de estado. Para obtener más información acerca de los objetos de estado, vea [Tabla de estado y Objetos de estado](status-table-and-status-objects.md).


- [Enviar o recibir un mensaje a petición:](sending-or-receiving-a-message-on-demand.md)describe cómo enviar o recibir un mensaje a petición.
    
- [Configuración del orden de](setting-transport-order.md)transporte: describe cómo establecer el orden de transporte.
    
- [Reconfigurar un proveedor de transporte:](reconfiguring-a-transport-provider.md)describe cómo reconfigurar un proveedor de transporte y qué propiedades están disponibles para establecer.
    

