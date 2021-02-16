---
title: Secuencias de llamada típicas de OSC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61960f7-e018-4d2e-8e32-426ed46d9064
description: En esta sección se describen las secuencias de llamada típicas de Outlook Social Connector (OSC) de miembros en las interfaces de extensibilidad del proveedor de OSC, que implementa un proveedor de OSC.
ms.openlocfilehash: f7829b710d6840ccd1fa0f990d6e03b2eb879431
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413615"
---
# <a name="osc-typical-calling-sequences"></a><span data-ttu-id="f1818-103">Secuencias de llamada típicas de OSC</span><span class="sxs-lookup"><span data-stu-id="f1818-103">OSC typical calling sequences</span></span>

<span data-ttu-id="f1818-104">En esta sección se describen las secuencias de llamada típicas de Outlook Social Connector (OSC) de miembros en las interfaces de extensibilidad del proveedor de OSC, que implementa un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="f1818-104">This section describes the Outlook Social Connector (OSC) typical calling sequences of members in the OSC provider extensibility interfaces, which an OSC provider implements.</span></span> <span data-ttu-id="f1818-105">Las secuencias de llamada típicas ilustran cómo y cuándo el OSC usa tales interfaces y métodos, para que te permita determinar mejor cómo implementar un miembro determinado en una interfaz de extensibilidad de proveedor.</span><span class="sxs-lookup"><span data-stu-id="f1818-105">The typical calling sequences illustrate how and when the OSC uses such interfaces and methods, to let you better determine how to implement a given member on a provider extensibility interface.</span></span> <span data-ttu-id="f1818-106">La secuencia de llamada real puede variar en función de las capacidades devueltas por el método [ISocialProvider::GetCapabilities.](isocialprovider-getcapabilities.md)</span><span class="sxs-lookup"><span data-stu-id="f1818-106">The actual calling sequence can vary depending on the capabilities returned by the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method.</span></span> <span data-ttu-id="f1818-107">Entre los ejemplos de funcionalidades se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f1818-107">Examples of capabilities include the following:</span></span> 
  
- <span data-ttu-id="f1818-108">Compatibilidad con proveedores para obtener, almacenar en caché o buscar dinámicamente amigos y actividades desde la red social.</span><span class="sxs-lookup"><span data-stu-id="f1818-108">Provider support for getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="f1818-109">Interfaz de usuario que debe mostrar el OSC para el inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="f1818-109">The user interface that the OSC should display for user logon.</span></span>
    
- <span data-ttu-id="f1818-110">El tipo de autenticación (por ejemplo, autenticación basada en formularios) que debe usar el OSC.</span><span class="sxs-lookup"><span data-stu-id="f1818-110">The authentication type (for example, forms-based authentication) that the OSC should use.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="f1818-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f1818-111">In this section</span></span>

- <span data-ttu-id="f1818-112">[Autenticación](basic-authentication.md)básica: describe la secuencia de llamada típica del OSC para admitir un usuario de Office que inicia sesión en una red social, si el proveedor de OSC admite la autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="f1818-112">[Basic Authentication](basic-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports basic authentication.</span></span>
    
- <span data-ttu-id="f1818-113">[](forms-based-authentication.md)Autenticación basada en formularios: describe la secuencia de llamada típica del OSC para admitir un usuario de Office que inicia sesión en una red social, si el proveedor de OSC admite la autenticación basada en formularios.</span><span class="sxs-lookup"><span data-stu-id="f1818-113">[Forms-Based Authentication](forms-based-authentication.md): Describes the typical calling sequence of the OSC to support an Office user who is logging on to a social network, if the OSC provider supports forms-based authentication.</span></span>
    
- <span data-ttu-id="f1818-114">[Obtener actividades:](getting-activities.md)describe la secuencia de llamada típica del OSC para sincronizar las actividades de los amigos del usuario de Office desde una red social, si el proveedor de OSC de red social admite la sincronización de actividades.</span><span class="sxs-lookup"><span data-stu-id="f1818-114">[Getting Activities](getting-activities.md): Describes the typical calling sequence of the OSC to synchronize the activities of the Office user's friends from a social network, if the social network OSC provider supports synchronization of activities.</span></span>
    
- <span data-ttu-id="f1818-115">[Obtener](getting-friends-information.md)información de amigos: describe la secuencia de llamadas típica del OSC para sincronizar la lista de amigos del usuario de Office desde una red social, si el proveedor de OSC de la red social admite la sincronización en caché de los contactos.</span><span class="sxs-lookup"><span data-stu-id="f1818-115">[Getting Friends Information](getting-friends-information.md): Describes the typical calling sequence of the OSC to synchronize the Office user's friends list from a social network, if the social network OSC provider supports cached synchronization of contacts.</span></span>
    
## <a name="reference"></a><span data-ttu-id="f1818-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="f1818-116">Reference</span></span>

- [<span data-ttu-id="f1818-117">Referencia del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="f1818-117">Outlook Social Connector Provider Reference</span></span>](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a><span data-ttu-id="f1818-118">Secciones relacionadas</span><span class="sxs-lookup"><span data-stu-id="f1818-118">Related sections</span></span>

- [<span data-ttu-id="f1818-119">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="f1818-119">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [<span data-ttu-id="f1818-120">Plantillas de ejemplo de OSC</span><span class="sxs-lookup"><span data-stu-id="f1818-120">OSC Sample Templates</span></span>](osc-sample-templates.md)
  
- [<span data-ttu-id="f1818-121">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="f1818-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)
  
- [<span data-ttu-id="f1818-122">Depurar un proveedor</span><span class="sxs-lookup"><span data-stu-id="f1818-122">Debugging a Provider</span></span>](debugging-a-provider.md)
  
- [<span data-ttu-id="f1818-123">Implementación de un proveedor</span><span class="sxs-lookup"><span data-stu-id="f1818-123">Deploying a Provider</span></span>](deploying-a-provider.md)
  
- [<span data-ttu-id="f1818-124">Procedimientos recomendados para desarrollar un proveedor</span><span class="sxs-lookup"><span data-stu-id="f1818-124">Best Practices for Developing a Provider</span></span>](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a><span data-ttu-id="f1818-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f1818-125">See also</span></span>

- [<span data-ttu-id="f1818-126">XML para funcionalidades</span><span class="sxs-lookup"><span data-stu-id="f1818-126">XML for Capabilities</span></span>](xml-for-capabilities.md)

