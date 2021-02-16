---
title: Información relativa a la OSC con Outlook y las redes sociales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y las actividades del panel de personas de Outlook, el estado o las actualizaciones de fotos de un compañero de trabajo, un amigo o cualquier persona con la que esté asociado.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428014"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="4c75c-103">Información relativa a la OSC con Outlook y las redes sociales</span><span class="sxs-lookup"><span data-stu-id="4c75c-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="4c75c-104">Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y las actividades del panel de personas de Outlook, el estado o las actualizaciones de fotos de un compañero de trabajo, un amigo o cualquier persona con la que esté asociado.</span><span class="sxs-lookup"><span data-stu-id="4c75c-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="4c75c-105">De forma predeterminada, el OSC muestra los correos electrónicos, los datos adjuntos y las solicitudes de reunión de Outlook recibidos de una persona seleccionada.</span><span class="sxs-lookup"><span data-stu-id="4c75c-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="4c75c-106">Si la persona seleccionada y el usuario de Office colaboran en un sitio de SharePoint, el OSC también muestra actualizaciones de documentos y otras actividades del sitio desde ese sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4c75c-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="4c75c-107">En función de los contextos de asociación que le interesan al usuario de Office, el usuario de Office puede instalar proveedores de OSC para aplicaciones de línea de negocio, sitios web corporativos internos o una variedad de sitios de redes sociales y profesionales, como LinkedIn, Facebook y Windows Live.</span><span class="sxs-lookup"><span data-stu-id="4c75c-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="4c75c-108">Para admitir el uso compartido de funciones entre aplicaciones cliente de Office, el motor principal de OSC se implementa como parte de un componente compartido de Office y el panel de personas se implementa como un complemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="4c75c-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="4c75c-109">Para usar el OSC, un usuario de Office debe haber instalado Outlook en ese equipo cliente y configurado Outlook con un perfil, para que el OSC pueda almacenar en caché los contactos de una carpeta Contactos.</span><span class="sxs-lookup"><span data-stu-id="4c75c-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="4c75c-110">Un proveedor de OSC es un ARCHIVO DLL del modelo de objetos componentes (COM) que permite que el OSC acceda a los datos de la red social de forma que sea independiente de las API de cada red social.</span><span class="sxs-lookup"><span data-stu-id="4c75c-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="4c75c-111">Una DLL del proveedor de OSC debe instalarse localmente en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="4c75c-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="4c75c-112">El proveedor de OSC de una red social conecta el OSC, que forma parte de Outlook, con la red social en Internet.</span><span class="sxs-lookup"><span data-stu-id="4c75c-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="4c75c-113">Un proveedor de OSC debe implementar un conjunto de interfaces, definidas como parte de la extensibilidad del proveedor de OSC, para comunicarse con el OSC.</span><span class="sxs-lookup"><span data-stu-id="4c75c-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="4c75c-114">La extensibilidad del proveedor de OSC está disponible como plataforma abierta.</span><span class="sxs-lookup"><span data-stu-id="4c75c-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="4c75c-115">La arquitectura del proveedor del OSC permite a varios proveedores trabajar con el motor principal de OSC y agregar información social como amigos y actividades.</span><span class="sxs-lookup"><span data-stu-id="4c75c-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="4c75c-116">La figura 1 ilustra la arquitectura del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="4c75c-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="4c75c-117">**Figura 1. Arquitectura de proveedor de Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="4c75c-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Redes sociales, proveedores de OSC, OSC y Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="4c75c-119">Terminología</span><span class="sxs-lookup"><span data-stu-id="4c75c-119">Terminology</span></span>

<span data-ttu-id="4c75c-120">En esta referencia de proveedor de Outlook Social Connector, se usa una red social para hacer referencia a los siguientes tipos de sitios:</span><span class="sxs-lookup"><span data-stu-id="4c75c-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="4c75c-121">Sitios de colaboración como SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4c75c-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="4c75c-122">Sitios de redes sociales como Facebook y Windows Live.</span><span class="sxs-lookup"><span data-stu-id="4c75c-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="4c75c-123">Sitios de red profesionales como LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="4c75c-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="4c75c-124">Otras aplicaciones de línea de negocio o sitios web internos corporativos usados para las redes.</span><span class="sxs-lookup"><span data-stu-id="4c75c-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="4c75c-125">El término friend se usa generalmente para incluir amigos, familiares, compañeros, conexiones y cualquier otra persona con la que un usuario de Office está asociado en un contexto de colaboración como SharePoint, o se ha agregado a la cuenta de red social del usuario.</span><span class="sxs-lookup"><span data-stu-id="4c75c-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="4c75c-126">Los que no son amigos son personas a las que se hace referencia en las actualizaciones de actividad de los amigos, pero no son amigos que se han agregado a la cuenta de red social del usuario de Office.</span><span class="sxs-lookup"><span data-stu-id="4c75c-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="4c75c-127">Los contactos son personas de una carpeta de contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="4c75c-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4c75c-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4c75c-128">See also</span></span>

- [<span data-ttu-id="4c75c-129">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="4c75c-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

