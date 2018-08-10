---
title: Información relativa a la OSC con Outlook y las redes sociales
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y panel de personas de Outlook actividades, estado o actualizaciones de fotografías para cualquier persona que está asociados con, amigo o un compañero de trabajo.
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821216"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="3f2a4-103">Información relativa a la OSC con Outlook y las redes sociales</span><span class="sxs-lookup"><span data-stu-id="3f2a4-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="3f2a4-104">Outlook Social Connector (OSC) puede mostrar en la tarjeta de contacto de Office y panel de personas de Outlook actividades, estado o actualizaciones de fotografías para cualquier persona que está asociados con, amigo o un compañero de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="3f2a4-105">De forma predeterminada, el OSC muestra los correos electrónicos de Outlook, los datos adjuntos, y las convocatorias de reunión reciben de una persona seleccionada.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="3f2a4-106">Si la persona seleccionada y el usuario de Office colaboran en un sitio de SharePoint, el OSC muestra también actualizaciones de documentos y otras actividades de sitio de ese sitio de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="3f2a4-107">Dependiendo de los contextos de asociación que es de interés para el usuario de Office, el usuario de Office puede instalar a proveedores de OSC para aplicaciones de línea de negocio, sitios Web corporativos interno o una variedad de sitios de red profesionales y sociales, como LinkedIn, Facebook y Windows Live.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="3f2a4-108">Para admitir el uso compartido de la funcionalidad a través de aplicaciones cliente de Office, el motor de núcleo OSC se implementa como parte de un componente compartido de Office y el panel de personas se implementa como un complemento de Outlook.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="3f2a4-109">Para usar el OSC, un usuario de Office debe tener instalado Outlook en el equipo cliente y configurar Outlook con un perfil, de modo que el OSC puede almacenar en caché los contactos en una carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="3f2a4-110">Un proveedor de OSC es un archivo DLL que permite el OSC tener acceso a datos de redes sociales de una forma que es independiente de la API de cada red social del modelo de objetos de componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="3f2a4-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="3f2a4-111">Un proveedor de OSC DLL debe instalarse localmente en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="3f2a4-112">Proveedor de OSC de una red social conecta el OSC, que es parte de Outlook, con las redes sociales en Internet.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="3f2a4-113">Un proveedor de OSC debe implementar un conjunto de interfaces, definido como parte de la extensibilidad del proveedor OSC, para comunicarse con el OSC.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="3f2a4-114">Extensibilidad de proveedores OSC está disponible como una plataforma abierta.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="3f2a4-115">La arquitectura de proveedor de la OSC permite varios proveedores para que funcione con el motor de núcleo OSC y agregar información sociales, como amigos y actividades.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="3f2a4-116">En la figura 1 ilustra la arquitectura de proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="3f2a4-117">**En la figura 1. Arquitectura de proveedor de Outlook Social Connector**</span><span class="sxs-lookup"><span data-stu-id="3f2a4-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![Redes sociales, proveedores de OSC, OSC y Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="3f2a4-119">Terminología</span><span class="sxs-lookup"><span data-stu-id="3f2a4-119">Terminology</span></span>

<span data-ttu-id="3f2a4-120">En esta referencia de proveedor de conector de Outlook Social, una red social se utiliza para hacer referencia a los siguientes tipos de sitios:</span><span class="sxs-lookup"><span data-stu-id="3f2a4-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="3f2a4-121">Sitios de colaboración, como SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="3f2a4-122">Sitios de redes sociales como Facebook y Windows Live.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="3f2a4-123">Sitios de red profesionales, como LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="3f2a4-124">Otras aplicaciones de línea de negocio o sitios Web corporativos internos utilizados redes.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="3f2a4-125">El amigo términos se usa generalmente para incluir amigos, familiares, compañeros de trabajo, las conexiones y cualquier otra persona está asociada con en un contexto de colaboración como SharePoint un usuario de Office, o ha agregado a la cuenta de usuario red social.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="3f2a4-126">No amigos son las personas que se hace referencia en las actualizaciones de actividad de amigos pero no amigos que se han agregado a la cuenta de red social del usuario de Office.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="3f2a4-127">Los contactos son personas en una carpeta de contactos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="3f2a4-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f2a4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f2a4-128">See also</span></span>

- [<span data-ttu-id="3f2a4-129">Introducción al desarrollo de un proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="3f2a4-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

