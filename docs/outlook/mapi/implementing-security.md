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
ms.openlocfilehash: c2926e7c94178d5a3135f34e2ab3b3ae11d145dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568486"
---
# <a name="implementing-security"></a><span data-ttu-id="9eb4f-103">Implementación de seguridad</span><span class="sxs-lookup"><span data-stu-id="9eb4f-103">Implementing Security</span></span>

  
  
<span data-ttu-id="9eb4f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9eb4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9eb4f-105">Si el sistema de mensajería lo requiere, el proveedor de transporte es responsable de implementar un nivel adecuado de seguridad para el acceso al sistema de mensajería.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="9eb4f-106">Cada mensaje entrante o saliente enviado a través de un proveedor de transporte por la cola MAPI se administra en el contexto de una sesión de inicio de sesión del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="9eb4f-107">El proveedor de transporte puede mostrar un cuadro de diálogo de inicio de sesión para el usuario que solicita las credenciales de un usuario antes de establecer una conexión de este tipo.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="9eb4f-108">Como alternativa, el proveedor de transporte puede almacenar las credenciales del usuario especificadas anteriormente en el intervalo de la propiedad segura dentro de una sección de perfil y usar para el acceso sin preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="9eb4f-109">Al implementar la seguridad de su proveedor de transporte, tenga en cuenta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9eb4f-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="9eb4f-110">Con varios proveedores de servicio instalado, puede haber una gran variedad de nombres y contraseñas asociadas a un usuario.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="9eb4f-111">MAPI permite varias sesiones con varias identidades.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="9eb4f-112">Los proveedores se recomienda para admitir varias sesiones pero no son necesarios para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="9eb4f-113">Cada sesión con un proveedor de transporte está asociada por MAPI con una sección discreta en el perfil del usuario.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="9eb4f-114">El proveedor de transporte puede usar el método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para obtener acceso a esta sección, que se puede utilizar para almacenar cualquier información asociada con esta sesión, incluidas las credenciales.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="9eb4f-115">Con varios proveedores de transporte instalados, no es necesariamente true que el usuario sólo tiene una dirección de correo electrónico única.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="9eb4f-116">Un usuario puede tener una dirección de correo electrónico independiente para cada proveedor de transporte instalada o puede tener una dirección distinta para cada sesión en un único proveedor.</span><span class="sxs-lookup"><span data-stu-id="9eb4f-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="9eb4f-117">Para obtener más información sobre cómo almacenar credenciales en secciones del perfil, vea [Servicios de mensajes y los perfiles](message-services-and-profiles.md) y [IProfSect: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="9eb4f-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

