---
title: Interfaces del proveedor de Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a sociales y las redes empresariales por lo que los usuarios pueden permanecer en contacto con las personas en sus redes sin salir de Office.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821210"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="cfc3b-103">Interfaces del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="cfc3b-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="cfc3b-104">Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a sociales y las redes empresariales por lo que los usuarios pueden permanecer en contacto con las personas en sus redes sin salir de Office.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="cfc3b-105">Un proveedor de OSC es un archivo DLL que permite el OSC tener acceso a datos de redes sociales de una forma que es independiente de la API de cada red social del modelo de objetos de componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="cfc3b-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="cfc3b-106">En la siguiente tabla se enumera las interfaces de extensibilidad del proveedor OSC.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="cfc3b-107">Debe implementar un proveedor de OSC cuatro de las cinco interfaces para comunicarse con el OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)y [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="cfc3b-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="cfc3b-108">Si el proveedor de OSC admite la sincronización de actividades, y a petición o sincronización híbrido de amigos, almacenamiento en caché las credenciales de inicio de sesión y registro uso en caché las credenciales o la capacidad que se deben seguir a una persona, el proveedor debe implementar [ISocialSession2 ](isocialsession2iunknown.md), así como.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="cfc3b-109">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="cfc3b-109">**Name**</span></span>|<span data-ttu-id="cfc3b-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cfc3b-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cfc3b-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="cfc3b-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="cfc3b-112">Representa a una persona en la red social.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="cfc3b-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="cfc3b-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="cfc3b-114">Representa el usuario ha iniciado la sesión.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="cfc3b-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="cfc3b-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="cfc3b-116">Representa una instancia de un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="cfc3b-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="cfc3b-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="cfc3b-118">Representa una conexión a un sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="cfc3b-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="cfc3b-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="cfc3b-120">Admite la sincronización de actividades, adición de amigos, sincronización a petición o híbrido de amigos o inicie sesión en la red social mediante el uso de credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="cfc3b-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

