---
title: Control de sesi�n MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3bc4aea5-ab01-4ba5-a4ad-7a9a76c6bf55
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 98c4bd0dba630db32fdb2309be3d29ebc13b1131
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422064"
---
# <a name="mapi-session-handling"></a>Control de sesi�n MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para poder comunicarse con proveedores de servicios y un sistema de mensajería subyacente, debe establecer una sesión. Una sesión MAPI es un vínculo de un cliente a otros componentes MAPI. Como resultado de iniciar correctamente una sesión, MAPI devuelve a los clientes un puntero a un objeto de sesión, un objeto que implementa la interfaz **IMAPISession.** Para obtener más información, [vea IMAPISession : IUnknown](imapisessioniunknown.md). Puede usar los métodos de la interfaz **IMAPISession** para obtener acceso a los objetos de los proveedores de libreta de direcciones y almacén de mensajes, obtener acceso a varias tablas, mostrar formularios, establecer propiedades del proveedor de transporte y realizar la administración de perfiles y servicios de mensajes. 
  
## <a name="in-this-section"></a>En esta sección

[Inicio de una sesión MAPI](starting-a-mapi-session.md)
  
> Describe cómo iniciar una sesión MAPI e incluye vínculos a temas con información más detallada.
    
[Finalización de una sesión MAPI](ending-a-mapi-session.md)
  
> Describe cómo finalizar una sesión MAPI.
    
[Acceso a objetos mediante el uso de la sesión](accessing-objects-by-using-the-session.md)
  
> Describe cómo usar un puntero de sesión para tener acceso a objetos de sesión.
    
[Recuperación de identidad principal y de proveedor](retrieving-primary-and-provider-identity.md)
  
> Describe las propiedades usadas para recuperar la identidad principal y del proveedor.
    
[Tabla de estado y objetos de estado](status-table-and-status-objects.md)
  
> Describe cómo obtener acceso a la información de la tabla de estado.
    

