---
title: Secuencias de llamada típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: En esta sección se describe las secuencias de llamada típicas de Outlook Social Connector (OSC) de los miembros de las interfaces de extensibilidad de proveedor OSC, que implementa un proveedor de OSC.
ms.openlocfilehash: 4a79e27fadb78933f41f26818cfab8b7f4a5aae7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821205"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="41a93-103">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="41a93-103">OSC typical calling sequences</span></span>

<span data-ttu-id="41a93-104">En esta sección se describe las secuencias de llamada típicas de Outlook Social Connector (OSC) de los miembros de las interfaces de extensibilidad de proveedor OSC, que implementa un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="41a93-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="41a93-105">Las secuencias de llamada típicas ilustran cómo y cuándo la OSC usa estas interfaces y métodos que permiten una mejor determinación del procedimiento para implementar un miembro dado en una interfaz de extensibilidad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="41a93-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="41a93-106">La secuencia de llamada real puede variar dependiendo de las capacidades devueltas por el método [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="41a93-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="41a93-107">Algunos ejemplos de capacidades son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="41a93-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="41a93-108">Proveedor de compatibilidad para obtener, almacenamiento en caché o buscar dinámicamente amigos y actividades de la red social.</span><span class="sxs-lookup"><span data-stu-id="41a93-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="41a93-109">La interfaz de usuario que se debe mostrar el OSC para inicio de sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="41a93-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="41a93-110">El tipo de autenticación (por ejemplo, la autenticación basada en formularios) que se debe usar el OSC.</span><span class="sxs-lookup"><span data-stu-id="41a93-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="41a93-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="41a93-111">In this section</span></span>

- <span data-ttu-id="41a93-112">[La autenticación básica](basic-authentication.md): describe la secuencia de llamada típica del OSC para admitir un usuario de Office que está iniciando sesión en una red social, si el proveedor OSC admite la autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="41a93-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="41a93-113">[Autenticación basada en formularios](forms-based-authentication.md): describe la secuencia de llamada típica del OSC para admitir un usuario de Office que está iniciando sesión en una red social, si el proveedor de OSC admite la autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="41a93-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="41a93-114">[Actividades de introducción](getting-activities.md): describe la secuencia de llamada típica del OSC para sincronizar las actividades de amigos del usuario de Office desde una red social, si el proveedor OSC de redes sociales admite la sincronización de actividades.</span><span class="sxs-lookup"><span data-stu-id="41a93-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="41a93-115">[Obtención de información sobre amigos](getting-friends-information.md): describe la secuencia de llamada típica del OSC para sincronizar la lista de amigos del usuario de Office desde una red social, si el proveedor OSC de redes sociales admite la sincronización en caché de los contactos.</span><span class="sxs-lookup"><span data-stu-id="41a93-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="41a93-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="41a93-116">Reference</span></span>

- [<span data-ttu-id="41a93-117">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="41a93-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="41a93-118">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="41a93-118">Related sections</span></span>

- [<span data-ttu-id="41a93-119">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="41a93-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="41a93-120">Plantillas de ejemplo OSC</span><span class="sxs-lookup"><span data-stu-id="41a93-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="41a93-121">Desarrollar un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="41a93-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="41a93-122">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="41a93-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="41a93-123">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="41a93-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="41a93-124">Prácticas recomendadas para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="41a93-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="41a93-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="41a93-125">See also</span></span>

- [<span data-ttu-id="41a93-126">XML de capacidades</span><span class="sxs-lookup"><span data-stu-id="41a93-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

