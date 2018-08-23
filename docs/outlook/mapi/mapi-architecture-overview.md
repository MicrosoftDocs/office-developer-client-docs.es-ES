---
title: Información general sobre la arquitectura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: a0f2efc17ca8790502f11d677498013cbe10205d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579357"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="b495f-103">Información general sobre la arquitectura MAPI</span><span class="sxs-lookup"><span data-stu-id="b495f-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="b495f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b495f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b495f-105">MAPI define una arquitectura modular, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="b495f-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="b495f-106">![Arquitectura de Outlook 2010] (media/amapi_43.gif "Arquitectura de Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="b495f-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="b495f-107">La aplicación de MAPI se conoce como una aplicación de cliente porque es un cliente del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="b495f-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="b495f-108">Las aplicaciones basadas en mensajería emplean mensajería como una parte central de su procesamiento y ofrecen una amplia características de mensajería, como el intercambio de información de diversos tipos en diversos formatos y la capacidad para guardar y organizar la información localmente.</span><span class="sxs-lookup"><span data-stu-id="b495f-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="b495f-109">Correo electrónico, programación, y las aplicaciones de flujo de trabajo son ejemplos de aplicaciones basadas en mensajería.</span><span class="sxs-lookup"><span data-stu-id="b495f-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="b495f-110">El subsistema MAPI se compone de una interfaz de usuario comunes y las interfaces de programación.</span><span class="sxs-lookup"><span data-stu-id="b495f-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="b495f-111">La interfaz de usuario comunes es un conjunto de cuadros de diálogo que le ofrece las aplicaciones cliente de un aspecto coherente y a los usuarios una manera coherente de trabajar.</span><span class="sxs-lookup"><span data-stu-id="b495f-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="b495f-112">MAPI tiene interfaces que se usan por el subsistema MAPI, por los programadores de software de cliente y los desarrolladores de proveedor de servicio de programación.</span><span class="sxs-lookup"><span data-stu-id="b495f-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="b495f-113">La interfaz de programación de MAPI es la interfaz de programación basada en objetos principal.</span><span class="sxs-lookup"><span data-stu-id="b495f-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="b495f-114">La interfaz de programación de MAPI es similar al modelo de objetos de OLE componente y se usa en el subsistema MAPI y las aplicaciones de cliente basadas en mensajería escritas en C o C++.</span><span class="sxs-lookup"><span data-stu-id="b495f-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="b495f-115">Como desarrollador de software de cliente, realizar llamadas MAPI directamente a través de la interfaz de programación de MAPI.</span><span class="sxs-lookup"><span data-stu-id="b495f-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="b495f-116">Puede implementar la mensajería con una sola interfaz de cliente MAPI o una combinación de interfaces.</span><span class="sxs-lookup"><span data-stu-id="b495f-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="b495f-117">Una sola aplicación puede realizar llamadas a métodos o funciones que pertenezcan a cualquiera de las interfaces.</span><span class="sxs-lookup"><span data-stu-id="b495f-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b495f-118">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b495f-118">See also</span></span>

<span data-ttu-id="b495f-119">-[Arquitectura y las características MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="b495f-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

