---
title: Implementación de la seguridad
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
# <a name="implementing-security"></a><span data-ttu-id="9ffe2-103">Implementación de la seguridad</span><span class="sxs-lookup"><span data-stu-id="9ffe2-103">Implementing Security</span></span>

  
  
<span data-ttu-id="9ffe2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ffe2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ffe2-105">Si el sistema de mensajería lo requiere, el proveedor de transporte es responsable de implementar un nivel de seguridad adecuado para el acceso al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="9ffe2-106">Cada mensaje entrante o saliente enviado a través de un proveedor de transporte por la cola MAPI se controla en el contexto de una sesión de inicio de sesión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="9ffe2-107">El proveedor de transporte puede mostrar un cuadro de diálogo de inicio de sesión al usuario que solicita las credenciales de un usuario antes de establecer dicha conexión.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="9ffe2-108">Como alternativa, el proveedor de transporte puede almacenar las credenciales especificadas anteriormente por el usuario en el rango de propiedades seguras dentro de una sección de perfil y usarlas para obtener acceso sin preguntar.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="9ffe2-109">Al implementar la seguridad del proveedor de transporte, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9ffe2-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="9ffe2-110">Con varios proveedores de servicios instalados, puede haber una gran variedad de nombres y contraseñas asociados con un usuario.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="9ffe2-111">MAPI permite varias sesiones con varias identidades.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="9ffe2-112">Se recomienda a los proveedores que admitan varias sesiones, pero no es necesario que lo hagan.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="9ffe2-113">Mapi asocia cada sesión con un proveedor de transporte con una sección discreta en el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="9ffe2-114">El proveedor de transporte puede usar el método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para obtener acceso a esta sección, que se puede usar para almacenar cualquier información asociada a esta sesión, incluidas las credenciales.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="9ffe2-115">Con varios proveedores de transporte instalados, no es necesariamente cierto que el usuario solo tenga una única dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="9ffe2-116">Un usuario puede tener una dirección de correo electrónico independiente para cada proveedor de transporte instalado o puede tener una dirección diferente para cada sesión en un único proveedor.</span><span class="sxs-lookup"><span data-stu-id="9ffe2-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="9ffe2-117">Para obtener más información acerca del almacenamiento de credenciales en las secciones de perfil, vea [Servicios](message-services-and-profiles.md) y perfiles de mensajes e [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="9ffe2-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

