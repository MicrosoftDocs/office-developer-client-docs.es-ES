---
title: Tratamiento de un proveedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567954"
---
# <a name="handling-a-transport-provider"></a>Tratamiento de un proveedor de transporte
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes se comuniquen con los proveedores de transporte a través de objetos de estado proporcionados por los proveedores de transporte y la cola de MAPI. Los clientes de acceso a objetos de estado mediante una llamada a [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar la tabla de estado. Objetos de estado implementan el [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) de la interfaz, que tiene métodos para configurar proveedores, vaciado entrante y saliente colas de mensajes, las contraseñas de configuración y validación de estado. Para obtener más información acerca de los objetos de estado, vea la [tabla de estado y objetos de estado](status-table-and-status-objects.md).


- [Enviar o recibir un mensaje de petición](sending-or-receiving-a-message-on-demand.md): se describe cómo enviar o recibir un mensaje de petición.
    
- [El orden de configuración de transporte](setting-transport-order.md): describe cómo establecer el orden de transporte.
    
- [Volver a configurar un proveedor de transporte](reconfiguring-a-transport-provider.md): se describe cómo volver a configurar un proveedor de transporte y qué propiedades están disponibles para establecer.
    

