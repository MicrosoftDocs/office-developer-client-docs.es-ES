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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410080"
---
# <a name="mapi-architecture-overview"></a><span data-ttu-id="a26af-103">Introducción a la arquitectura MAPI</span><span class="sxs-lookup"><span data-stu-id="a26af-103">MAPI architecture overview</span></span>
 
<span data-ttu-id="a26af-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a26af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a26af-105">MAPI define una arquitectura modular, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="a26af-105">MAPI defines a modular architecture, as shown in the following illustration.</span></span>  
  
<span data-ttu-id="a26af-106">![Outlook arquitectura de 2010 Outlook](media/amapi_43.gif "arquitectura de 2010")</span><span class="sxs-lookup"><span data-stu-id="a26af-106">![Outlook 2010 architecture](media/amapi_43.gif "Outlook 2010 architecture")</span></span>
  
<span data-ttu-id="a26af-107">La aplicación MAPI se conoce como una aplicación cliente porque es un cliente del subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="a26af-107">The MAPI application is known as a client application because it is a client of the MAPI subsystem.</span></span> <span data-ttu-id="a26af-108">Las aplicaciones basadas en mensajería emplean la mensajería como parte central de su procesamiento y ofrecen amplias características de mensajería, como el intercambio de información de varios tipos en varios formatos y la capacidad de guardar y organizar la información localmente.</span><span class="sxs-lookup"><span data-stu-id="a26af-108">Messaging-based applications employ messaging as a central part of their processing and offer extensive messaging features, such as the exchange of information of various types in various formats and the ability to save and organize the information locally.</span></span> <span data-ttu-id="a26af-109">Las aplicaciones de correo electrónico, programación y flujo de trabajo son ejemplos de aplicaciones basadas en mensajería.</span><span class="sxs-lookup"><span data-stu-id="a26af-109">Email, scheduling, and work flow applications are examples of messaging-based applications.</span></span>
  
<span data-ttu-id="a26af-110">El subsistema MAPI está hecho de una interfaz de usuario común y las interfaces de programación.</span><span class="sxs-lookup"><span data-stu-id="a26af-110">The MAPI subsystem is made up of a common user interface and the programming interfaces.</span></span> <span data-ttu-id="a26af-111">La interfaz de usuario común es un conjunto de cuadros de diálogo que proporciona a las aplicaciones cliente una apariencia coherente y a los usuarios una forma coherente de trabajar.</span><span class="sxs-lookup"><span data-stu-id="a26af-111">The common user interface is a set of dialog boxes that gives client applications a consistent look and users a consistent way to work.</span></span>
  
<span data-ttu-id="a26af-112">MAPI tiene interfaces de programación que usan el subsistema MAPI, los programadores de software cliente y los desarrolladores de proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="a26af-112">MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers.</span></span> <span data-ttu-id="a26af-113">La interfaz de programación MAPI es la interfaz de programación principal basada en objetos.</span><span class="sxs-lookup"><span data-stu-id="a26af-113">The MAPI programming interface is the main object-based programming interface.</span></span> <span data-ttu-id="a26af-114">La interfaz de programación MAPI es similar al modelo de objetos de componente OLE y la usan el subsistema MAPI y las aplicaciones cliente basadas en mensajería escritas en C o C++.</span><span class="sxs-lookup"><span data-stu-id="a26af-114">The MAPI programming interface is similar to the OLE Component Object Model and is used by the MAPI subsystem and messaging-based client applications written in C or C++.</span></span> 
  
<span data-ttu-id="a26af-115">Como desarrollador de software cliente, realiza llamadas MAPI directamente a través de la interfaz de programación MAPI.</span><span class="sxs-lookup"><span data-stu-id="a26af-115">As a client software developer, you make MAPI calls directly through the MAPI programming interface.</span></span> <span data-ttu-id="a26af-116">Puede implementar la mensajería con una única interfaz de cliente MAPI o una combinación de interfaces.</span><span class="sxs-lookup"><span data-stu-id="a26af-116">You can implement messaging with a single MAPI client interface or a combination of interfaces.</span></span> <span data-ttu-id="a26af-117">Una sola aplicación puede realizar llamadas a métodos o funciones pertenecientes a cualquiera de las interfaces.</span><span class="sxs-lookup"><span data-stu-id="a26af-117">A single application can make calls to methods or functions belonging to any of the interfaces.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a26af-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a26af-118">See also</span></span>

<span data-ttu-id="a26af-119">-[Características y arquitectura mapi](mapi-features-and-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="a26af-119">-[MAPI features and architecture](mapi-features-and-architecture.md)</span></span>

