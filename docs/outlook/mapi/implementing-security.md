---
title: Implementar la seguridad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417290"
---
# <a name="implementing-security"></a>Implementar la seguridad

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Si el sistema de mensajería lo requiere, el proveedor de transporte es responsable de implementar un nivel de seguridad adecuado para el acceso al sistema de mensajería. Cada mensaje entrante o saliente enviado a través de un proveedor de transporte por la cola MAPI se controla en el contexto de una sesión de inicio de sesión del proveedor. El proveedor de transporte puede mostrar un cuadro de diálogo de inicio de sesión al usuario que solicite las credenciales de un usuario antes de establecer dicha conexión. Como alternativa, el proveedor de transporte puede almacenar las credenciales especificadas anteriormente del usuario en el intervalo de propiedades seguras dentro de una sección de perfil y usarlas para obtener acceso sin preguntar.
  
Al implementar la seguridad del proveedor de transporte, tenga en cuenta lo siguiente:
  
- Con varios proveedores de servicios instalados, puede haber una gran variedad de nombres y contraseñas asociados con un usuario.
    
- MAPI permite varias sesiones con varias identidades. Se recomienda a los proveedores que admitan varias sesiones, pero no es necesario hacerlo.
    
- Mapi asocia cada sesión con un proveedor de transporte con una sección discreta en el perfil del usuario. El proveedor de transporte puede usar el método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para obtener acceso a esta sección, que se puede usar para almacenar cualquier información asociada a esta sesión, incluidas las credenciales. 
    
- Con varios proveedores de transporte instalados, no es necesariamente cierto que el usuario solo tenga una sola dirección de correo electrónico. Un usuario puede tener una dirección de correo electrónico independiente para cada proveedor de transporte instalado o puede tener una dirección diferente para cada sesión en un único proveedor.
    
Para obtener más información acerca del almacenamiento de credenciales en las secciones de perfil, vea [Message Services and Profiles](message-services-and-profiles.md) e [IProfSect : IMAPIProp](iprofsectimapiprop.md).
  

