---
title: Introducción a la arquitectura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297896"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="c02bd-103">Introducción a la arquitectura MAPI</span><span class="sxs-lookup"><span data-stu-id="c02bd-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="c02bd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c02bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c02bd-105">MAPI define una arquitectura modular, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="c02bd-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="c02bd-106">![Arquitectura de Outlook 2010] (media/amapi_43.gif "Arquitectura de Outlook 2010")</span><span class="sxs-lookup"><span data-stu-id="c02bd-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="c02bd-107">La aplicación MAPI se conoce como una aplicación cliente porque es un cliente del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="c02bd-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="c02bd-108">Las aplicaciones basadas en mensajería usan la mensajería como parte central de su procesamiento y ofrecen amplias características de mensajería, como el intercambio de información de distintos tipos en distintos formatos y la capacidad de guardar y organizar la información de forma local.</span><span class="sxs-lookup"><span data-stu-id="c02bd-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="c02bd-109">Las aplicaciones de correo electrónico, programación y flujo de trabajo son ejemplos de aplicaciones basadas en mensajería.</span><span class="sxs-lookup"><span data-stu-id="c02bd-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="c02bd-110">El subsistema MAPI consta de una interfaz de usuario común y de las interfaces de programación.</span><span class="sxs-lookup"><span data-stu-id="c02bd-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="c02bd-111">La interfaz de usuario común es un conjunto de cuadros de diálogo que da a las aplicaciones cliente un aspecto coherente y a los usuarios una forma coherente de trabajar.</span><span class="sxs-lookup"><span data-stu-id="c02bd-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="c02bd-112">MAPI tiene interfaces de programación usadas por el subsistema MAPI, por desarrolladores de software de cliente y por programadores de proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="c02bd-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="c02bd-113">La interfaz de programación de MAPI es la interfaz de programación basada en objetos principal.</span><span class="sxs-lookup"><span data-stu-id="c02bd-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="c02bd-114">La interfaz de programación de MAPI es similar al modelo de objetos de componentes OLE y se usa en el subsistema MAPI y en las aplicaciones cliente basadas en mensajería escritas en C o C++.</span><span class="sxs-lookup"><span data-stu-id="c02bd-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="c02bd-115">Como desarrollador de software de cliente, realiza llamadas MAPI directamente a través de la interfaz de programación MAPI.</span><span class="sxs-lookup"><span data-stu-id="c02bd-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="c02bd-116">Puede implementar la mensajería con una única interfaz de cliente MAPI o con una combinación de interfaces.</span><span class="sxs-lookup"><span data-stu-id="c02bd-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="c02bd-117">Una sola aplicación puede realizar llamadas a métodos o funciones pertenecientes a cualquiera de las interfaces.</span><span class="sxs-lookup"><span data-stu-id="c02bd-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c02bd-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c02bd-118">See also</span></span>

<span data-ttu-id="c02bd-119">-[Arquitectura y características de MAPI](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="c02bd-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

