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
ms.openlocfilehash: cdf3052175870287ff1a66d3745e90f8b8fff256
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818210"
---
# <a name="mapi-session-handling"></a>Control de sesi�n MAPI

  
  
**Hace referencia a**: Outlook 
  
Para poder comunicarse con proveedores de servicios y un sistema de mensajería subyacente, debe establecer una sesión. Una sesión MAPI es un vínculo desde un cliente a otros componentes MAPI. Como resultado de inicio de una sesión correctamente, MAPI devuelve a los clientes un puntero a un objeto de sesión, un objeto que implementa la interfaz **IMAPISession** . Para obtener más información, vea [IMAPISession: IUnknown](imapisessioniunknown.md). Puede usar los métodos de la interfaz **IMAPISession** para tener acceso a los objetos de proveedores de almacenes de libreta de direcciones y el mensaje de dirección, obtener acceso a varias tablas, mostrar formularios, establecer propiedades del proveedor de transporte y realizar la administración del servicio de perfil y el mensaje. 
  
## <a name="in-this-section"></a>En esta sección

[Iniciar una sesión MAPI](starting-a-mapi-session.md)
  
> Describe cómo iniciar una sesión MAPI e incluye vínculos a temas con información más detallada.
    
[Finalizar una sesión MAPI](ending-a-mapi-session.md)
  
> Se describe cómo finalizar una sesión de MAPI.
    
[Obtener acceso a los objetos con la sesión](accessing-objects-by-using-the-session.md)
  
> Describe cómo utilizar un puntero de sesión para tener acceso a objetos de la sesión.
    
[Recuperar identidades de proveedor y principales](retrieving-primary-and-provider-identity.md)
  
> Se describen las propiedades que se usan para recuperar principal y la identidad del proveedor.
    
[Tabla de estado y objetos de estado](status-table-and-status-objects.md)
  
> Describe cómo obtener acceso a información desde la tabla de estado.
    

