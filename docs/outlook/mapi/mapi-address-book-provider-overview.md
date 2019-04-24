---
title: Introducción al proveedor de libreta de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298148"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="696c8-103">Introducción al proveedor de libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="696c8-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="696c8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="696c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="696c8-105">Los proveedores de la libreta de direcciones administran el acceso a la información del directorio.</span><span class="sxs-lookup"><span data-stu-id="696c8-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="696c8-106">La información de directorio consta de los datos para dos tipos de destinatarios de mensajes: usuarios de mensajería individuales y grupos de usuarios de mensajería que se suelen tratar juntos en listas de distribución.</span><span class="sxs-lookup"><span data-stu-id="696c8-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="696c8-107">Según el tipo de destinatario y el proveedor de la libreta de direcciones, existe una amplia variedad de información que puede estar disponible.</span><span class="sxs-lookup"><span data-stu-id="696c8-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="696c8-108">Por ejemplo, todos los proveedores de la libreta de direcciones almacenan el nombre, la dirección y el tipo de dirección de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="696c8-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="696c8-109">Cada proveedor de la libreta de direcciones organiza estos datos mediante uno o varios contenedores.</span><span class="sxs-lookup"><span data-stu-id="696c8-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="696c8-110">El número y la estructura de los contenedores depende de la implementación del proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="696c8-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="696c8-111">Por ejemplo, un proveedor de la libreta de direcciones puede usar un único contenedor para contener toda la información, otro puede usar un contenedor de nivel superior que contenga subcontenedores y un tercero puede usar varios contenedores de nivel superior, cada uno de los cuales contiene subcontenedores.</span><span class="sxs-lookup"><span data-stu-id="696c8-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="696c8-112">Una jerarquía de contenedores de libretas de direcciones puede ser bastante profunda; no hay ningún límite en el número de subcontenedores que se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="696c8-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="696c8-113">En la siguiente ilustración se muestra una organización típica de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="696c8-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="696c8-114">**Organización de la libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="696c8-114">**Address book organization**</span></span>
  
<span data-ttu-id="696c8-115">![Organización] de la libreta de direcciones (media/amapi_04.gif "Organización") de la libreta de direcciones</span><span class="sxs-lookup"><span data-stu-id="696c8-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="696c8-116">MAPI integra toda la información proporcionada por los proveedores de libreta de direcciones instalados en una única libreta de direcciones, que presenta una vista unificada de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="696c8-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="696c8-117">La lista integrada muestra los contenedores de nivel superior que se muestran en cada uno de los proveedores de libreta de direcciones instalados.</span><span class="sxs-lookup"><span data-stu-id="696c8-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="696c8-118">La mayoría de los proveedores de libreta de direcciones solo exponen unos pocos contenedores (normalmente uno a tres) en el nivel superior para la inclusión en el nivel superior de la libreta de direcciones MAPI integrada.</span><span class="sxs-lookup"><span data-stu-id="696c8-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="696c8-119">Por ejemplo, un proveedor de libreta de direcciones podría poner a disposición "todos los usuarios" y "usuarios locales" como dos contenedores en el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="696c8-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="696c8-120">Los usuarios de las aplicaciones cliente pueden ver el contenido de los contenedores de la libreta de direcciones y, en algunos casos, modificar su contenido.</span><span class="sxs-lookup"><span data-stu-id="696c8-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="696c8-121">Los contenedores de la libreta de direcciones se pueden crear con distintos niveles de acceso, según el proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="696c8-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="696c8-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="696c8-122">See also</span></span>

- [<span data-ttu-id="696c8-123">Arquitectura y características de MAPI</span><span class="sxs-lookup"><span data-stu-id="696c8-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

