---
title: Interfaces de proveedor de Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a redes sociales y empresariales para que los usuarios puedan estar en contacto con las personas de sus redes sin salir de Office.
ms.openlocfilehash: 77759db34f63239473e0682cfaca720860e96768
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359853"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="1b01d-103">Interfaces de proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="1b01d-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="1b01d-104">Outlook Social Connector (OSC) es una característica de Office compartida por las aplicaciones cliente de Office que se conecta a redes sociales y empresariales para que los usuarios puedan estar en contacto con las personas de sus redes sin salir de Office.</span><span class="sxs-lookup"><span data-stu-id="1b01d-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="1b01d-105">Un proveedor OSC es un archivo DLL del modelo de objetos componentes (COM) que permite al OSC tener acceso a los datos de la red social de manera independiente de las API de cada red social.</span><span class="sxs-lookup"><span data-stu-id="1b01d-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="1b01d-106">En la siguiente tabla se enumeran las interfaces de la extensibilidad del proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="1b01d-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="1b01d-107">Un proveedor OSC debe implementar cuatro de las cinco interfaces para comunicarse con el OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)y [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1b01d-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="1b01d-108">Si el proveedor de OSC admite la sincronización de actividades, la sincronización híbrida o a petición de amigos, el almacenamiento en caché de credenciales de inicio de sesión y el inicio de sesión con credenciales almacenadas en caché, o la posibilidad de seguir a una persona, el proveedor debe implementar [ISocialSession2 ](isocialsession2iunknown.md), también.</span><span class="sxs-lookup"><span data-stu-id="1b01d-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="1b01d-109">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1b01d-109">**Name**</span></span>|<span data-ttu-id="1b01d-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1b01d-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b01d-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="1b01d-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="1b01d-112">Representa una persona de la red social.</span><span class="sxs-lookup"><span data-stu-id="1b01d-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="1b01d-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="1b01d-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="1b01d-114">Representa el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="1b01d-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="1b01d-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="1b01d-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="1b01d-116">Representa una instancia de un proveedor de OSC.</span><span class="sxs-lookup"><span data-stu-id="1b01d-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="1b01d-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="1b01d-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="1b01d-118">Representa una conexión a un sitio de red social.</span><span class="sxs-lookup"><span data-stu-id="1b01d-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="1b01d-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="1b01d-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="1b01d-120">Admite la sincronización de actividades, la adición de amigos, la sincronización a petición o la sincronización híbrida de amigos o el inicio de sesión en la red social mediante el uso de credenciales almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="1b01d-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

