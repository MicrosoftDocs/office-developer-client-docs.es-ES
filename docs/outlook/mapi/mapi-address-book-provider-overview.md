---
title: Introducción al proveedor de la libreta de direcciones MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4bd64aadd5fc18ba79a8717a5c58df72cd3695ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818061"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="13555-103">Introducción al proveedor de la libreta de direcciones MAPI</span><span class="sxs-lookup"><span data-stu-id="13555-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="13555-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13555-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13555-105">Libreta de direcciones de proveedores de controlar el acceso a información de Active directory.</span><span class="sxs-lookup"><span data-stu-id="13555-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="13555-106">Información de Active Directory se compone de datos para dos tipos de destinatarios del mensaje: individuales de los usuarios y grupos de usuarios de mensajería que con frecuencia se tratan juntos en las listas de distribución de mensajería.</span><span class="sxs-lookup"><span data-stu-id="13555-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="13555-107">Según el tipo de destinatario y el proveedor de la libreta de direcciones, hay una amplia variedad de información que puede estar disponible.</span><span class="sxs-lookup"><span data-stu-id="13555-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="13555-108">Por ejemplo, todos los proveedores de libreta de direcciones almacenan nombre, dirección y tipo de dirección de un destinatario.</span><span class="sxs-lookup"><span data-stu-id="13555-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="13555-109">Cada proveedor de la libreta de direcciones organiza estos datos mediante el uso de uno o varios contenedores.</span><span class="sxs-lookup"><span data-stu-id="13555-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="13555-110">El número y la estructura de los contenedores depende de la implementación del proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="13555-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="13555-111">Por ejemplo, un proveedor de libreta de direcciones podría usar un único contenedor para contener toda la información, otro podría usar un contenedor de nivel superior que contiene los subcontenedores y una tercera podría usar varios contenedores de nivel superior, cada subcontenedores de explotación.</span><span class="sxs-lookup"><span data-stu-id="13555-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="13555-112">Una jerarquía de contenedor de la libreta de direcciones puede ser un proceso bastante profunda; No hay ningún límite para el número de subcontenedores que se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="13555-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="13555-113">En la siguiente ilustración muestra una organización típica de la libreta de direcciones MAPI.</span><span class="sxs-lookup"><span data-stu-id="13555-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="13555-114">**Organización de la libreta de direcciones**</span><span class="sxs-lookup"><span data-stu-id="13555-114">**Address book organization**</span></span>
  
<span data-ttu-id="13555-115">![Organización de la libreta de direcciones] (media/amapi_04.gif "Organización de la libreta de direcciones")</span><span class="sxs-lookup"><span data-stu-id="13555-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="13555-116">MAPI integra toda la información proporcionada por los proveedores de la libreta de direcciones instalado en una sola libreta de direcciones, presentar una vista unificada a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="13555-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="13555-117">La lista integrada muestra los contenedores de nivel superior que se muestra en cada uno de los proveedores de la libreta de direcciones instalado.</span><span class="sxs-lookup"><span data-stu-id="13555-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="13555-118">La mayoría de los proveedores de la libreta de direcciones exponen solo unos contenedores (normalmente, uno a tres) en el nivel superior para su inclusión en el nivel superior de la libreta de direcciones integrada de MAPI.</span><span class="sxs-lookup"><span data-stu-id="13555-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="13555-119">Por ejemplo, un proveedor de la libreta de direcciones podría realizar disponibles "Todos los usuarios" y "Usuarios locales" como dos contenedores en el nivel superior.</span><span class="sxs-lookup"><span data-stu-id="13555-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="13555-120">Los usuarios de las aplicaciones cliente pueden ver el contenido de los contenedores de la libreta de direcciones y, en algunos casos, modifique el contenido.</span><span class="sxs-lookup"><span data-stu-id="13555-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="13555-121">Contenedores de la libreta de direcciones se pueden crear con distintos niveles de acceso, según el proveedor de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="13555-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13555-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="13555-122">See also</span></span>

- [<span data-ttu-id="13555-123">Arquitectura y las características MAPI</span><span class="sxs-lookup"><span data-stu-id="13555-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

