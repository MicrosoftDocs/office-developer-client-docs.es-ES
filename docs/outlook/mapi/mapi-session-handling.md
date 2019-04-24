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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328227"
---
# <a name="mapi-session-handling"></a>Control de sesi�n MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Antes de poder comunicarse con proveedores de servicios y un sistema de mensajería subyacente, debe establecer una sesión. Una sesión MAPI es un vínculo entre un cliente y otros componentes de MAPI. Como resultado de iniciar una sesión correctamente, MAPI vuelve a los clientes un puntero a un objeto de sesión (un objeto que implementa la interfaz **IMAPISession** . Para obtener más información, vea [IMAPISession: IUnknown](imapisessioniunknown.md). Puede usar los métodos de la interfaz **IMAPISession** para tener acceso a los objetos de la libreta de direcciones y los proveedores de almacenamiento de mensajes, tener acceso a varias tablas, Mostrar formularios, establecer las propiedades de los proveedores de transporte y realizar la administración de perfiles y del servicio de mensajes. 
  
## <a name="in-this-section"></a>En esta sección

[Inicio de una sesión MAPI](starting-a-mapi-session.md)
  
> Describe cómo iniciar una sesión MAPI e incluye vínculos a temas con información más detallada.
    
[Finalizar una sesión MAPI](ending-a-mapi-session.md)
  
> Describe cómo finalizar una sesión MAPI.
    
[Obtener acceso a objetos mediante la sesión](accessing-objects-by-using-the-session.md)
  
> Describe cómo utilizar un puntero de sesión para tener acceso a objetos de sesión.
    
[Recuperación de la identidad principal y del proveedor](retrieving-primary-and-provider-identity.md)
  
> Describe las propiedades usadas para recuperar la identidad del proveedor y la principal.
    
[Tabla de estado y objetos de estado](status-table-and-status-objects.md)
  
> Describe cómo tener acceso a la información de la tabla de estado.
    

