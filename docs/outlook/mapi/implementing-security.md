---
title: Implementación de seguridad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310062"
---
# <a name="implementing-security"></a>Implementación de seguridad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si el sistema de mensajería lo requiere, el proveedor de transporte es responsable de implementar un nivel adecuado de seguridad para el acceso al sistema de mensajería. Todos los mensajes entrantes o salientes que se envían a través de un proveedor de transporte por la cola MAPI se controlan en el contexto de una sesión de inicio de sesión del proveedor. El proveedor de transporte puede mostrar un cuadro de diálogo de inicio de sesión al usuario que solicita las credenciales de un usuario antes de establecer dicha conexión. Como alternativa, el proveedor de transporte puede almacenar las credenciales especificadas previamente del usuario en el intervalo de propiedades seguras dentro de una sección de perfil y usarlas para Access sin pedir confirmación.
  
Al implementar la seguridad del proveedor de transporte, tenga en cuenta lo siguiente:
  
- Con varios proveedores de servicios instalados, puede haber una multitud de nombres y contraseñas asociados con un usuario.
    
- MAPI permite varias sesiones con varias identidades. Se recomienda a los proveedores que admitan varias sesiones pero no son necesarias para ello.
    
- Cada sesión con un proveedor de transporte está asociada por MAPI con una sección discreta en el perfil del usuario. El proveedor de transporte puede usar el método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) para obtener acceso a esta sección, que se puede usar para almacenar cualquier información asociada a esta sesión, incluidas las credenciales. 
    
- Con varios proveedores de transporte instalados, no es necesariamente cierto que el usuario solo tiene una dirección de correo electrónico única. Un usuario puede tener una dirección de correo electrónico independiente para cada proveedor de transporte instalado o puede tener una dirección diferente para cada sesión en un único proveedor.
    
Para obtener más información sobre el almacenamiento de credenciales en secciones de perfil, vea [servicios y perfiles de mensajes](message-services-and-profiles.md) y [IProfSect: IMAPIProp](iprofsectimapiprop.md).
  

